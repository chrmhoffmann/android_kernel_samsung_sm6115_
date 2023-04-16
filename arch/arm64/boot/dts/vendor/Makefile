WT_FEATURE_ENABLE_DTC :=
ifeq ($(CONFIG_WT_BOOTLOADER_LOG),y)
WT_FEATURE_ENABLE_DTC += -DWT_BOOTLOADER_LOG
endif
ifeq ($(CONFIG_WT_BOOT_REASON),y)
WT_FEATURE_ENABLE_DTC += -DWT_BOOT_REASON
endif
ifeq ($(CONFIG_WT_SYSTEM_MONITOR),y)
WT_FEATURE_ENABLE_DTC += -DWT_SYSTEM_MONITOR
endif

ifeq ($(CONFIG_BUILD_ARM64_DT_OVERLAY),y)
        dtbo-$(CONFIG_ARCH_BENGAL) += \
                P85946-qrd-overlay.dtbo \

P85946-qrd-overlay.dtbo-base := bengal.dtb
else
dtb-$(CONFIG_ARCH_BENGAL) += bengal-qrd.dtb
endif

always		:= $(dtb-y)
subdir-y	:= $(dts-dirs)
clean-files    := *.dtb *.dtbo
