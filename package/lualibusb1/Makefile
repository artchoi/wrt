include $(TOPDIR)/rules.mk

PKG_NAME:=lualibusb1
PKG_VERSION:=1.0.1

PKG_SOURCE_URL:=http://$(PKG_NAME).googlecode.com/files
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz

include $(INCLUDE_DIR)/package.mk

define Package/lualibusb1
  SUBMENU:=Lua
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=libusb Lua binding
  MAINTAINER:=Oleksandr Grytsenko <grytole@gmail.com>
  DEPENDS:=+liblua +libusb-1.0
endef

define Package/lualibusb1/description
  This is the Lua binding for the libusb-1.0 library.
endef

define Package/lualibusb1/install
	$(INSTALL_DIR) $(1)/usr/lib/lua
	$(INSTALL_BIN) $(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)/libusb1.so $(1)/usr/lib/lua/libusb1.so
endef

$(eval $(call BuildPackage,lualibusb1))
