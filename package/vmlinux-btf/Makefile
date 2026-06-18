include $(TOPDIR)/rules.mk

PKG_NAME:=vmlinux-btf
PKG_VERSION:=1.0
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/vmlinux-btf
  SECTION:=base
  CATEGORY:=Base system
  TITLE:=Dummy vmlinux-btf for dependencies
endef

define Package/vmlinux-btf/description
  A dummy package that satisfies the vmlinux-btf dependency for daed.
  Since BTF is built into the kernel natively in this firmware, this 
  prevents opkg errors when users update packages from external feeds.
endef

define Build/Prepare
endef

define Build/Compile
endef

define Package/vmlinux-btf/install
	$(INSTALL_DIR) $(1)/etc
	echo "This is a dummy package to satisfy opkg dependencies. BTF is native." > $(1)/etc/vmlinux-btf.dummy
endef

$(eval $(call BuildPackage,vmlinux-btf))
