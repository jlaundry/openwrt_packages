include $(TOPDIR)/rules.mk

PKG_NAME:=fluent-bit
PKG_VERSION:=2.2.0
PKG_RELEASE:=1

PKG_SOURCE:=v$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/fluent/fluent-bit/archive/refs/tags/
PKG_HASH:=c02497f95e5455c5cd587a00efe9d919ac6d0a7d26ad6b5320b25bbc664c04cd

PKG_MAINTAINER:=Jed Laundry <openwrt@jlaundry.nz>
PKG_LICENSE:=Apache-2.0

PKG_FIXUP:=autoreconf

include $(INCLUDE_DIR)/package.mk

define Package/fluent-bit
  SECTION:=utils
  CATEGORY:=Utilities
  DEPENDS:=
  TITLE:=Logging and metrics processor and forwarder
  URL:=https://fluentbit.io/
endef

define Package/fluent-bit/description
	Fluent Bit is an open-source telemetry agent specifically designed to
	efficiently handle the challenges of collecting and processing telemetry
	data across a wide range of environments, from constrained systems to
	complex cloud infrastructures.
endef

define Package/fluent-bit/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/fluent-bit $(1)/usr/bin/
endef

$(eval $(call BuildPackage,fluent-bit))
