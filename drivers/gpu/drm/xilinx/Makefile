#
# Makefile for the drm device driver.  This driver provides support for the
# Direct Rendering Infrastructure (DRI) in XFree86 4.1.0 and higher.

ccflags-y := -I$(src)

MIXER_CRTC_DRM=crtc/mixer/drm
MIXER_CRTC_HW=crtc/mixer/hw

xilinx_drm-y := xilinx_drm_crtc.o xilinx_drm_connector.o xilinx_drm_drv.o \
		xilinx_drm_encoder.o xilinx_drm_fb.o xilinx_drm_gem.o \
		xilinx_drm_plane.o
xilinx_drm-y += xilinx_cresample.o xilinx_osd.o xilinx_rgb2yuv.o xilinx_vtc.o
xilinx_drm-$(CONFIG_DRM_XILINX_MIXER) += $(MIXER_CRTC_HW)/xilinx_mixer_hw.o
xilinx_drm-$(CONFIG_DRM_XILINX_MIXER) += $(MIXER_CRTC_DRM)/xilinx_drm_mixer.o

obj-$(CONFIG_DRM_XILINX) += xilinx_drm.o
obj-$(CONFIG_DRM_XILINX_DP) += xilinx_drm_dp.o
obj-$(CONFIG_DRM_XILINX_DP_SUB) += xilinx_drm_dp_sub.o
