---
UID: TP:wcn
ms.assetid: 0f160390-e9fe-3eb7-acb4-311e3c3278c6
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Windows Connect Now

## -description

Overview of the Windows Connect Now technology.

To develop Windows Connect Now, you need these headers:

 * [wcndevice.h](../wcndevice/index.md)
 * [wcntypes.h](../wcntypes/index.md)

For the programming guide, see [Windows Connect Now](/windows/desktop/wcn).

## Structures

| Title   | Description   |
| ---- |:---- |
| [tagWCN_VALUE_TYPE_PRIMARY_DEVICE_TYPE structure](..\wcntypes\ns-wcntypes-tagwcn_value_type_primary_device_type.md) | WCN_VALUE_TYPE_PRIMARY_DEVICE_TYPE structure contains information that identifies the device type by category, sub-category, and a manufacturer specific OUI (Organization ID). |
| [tagWCN_VENDOR_EXTENSION_SPEC structure](..\wcndevice\ns-wcndevice-tagwcn_vendor_extension_spec.md) | WCN_VENDOR_EXTENSION_SPEC structure contains data that defines a vendor extension. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [tagWCN_ATTRIBUTE_TYPE enumeration](..\wcntypes\ne-wcntypes-tagwcn_attribute_type.md) | WCN_ATTRIBUTE_TYPE enumeration defines the attribute buffer types defined for Wi-Fi Protected Setup. The overall size occupied by each attribute buffer includes an additional 4 bytes (2 bytes of ID, 2 bytes of Length). |
| [tagWCN_PASSWORD_TYPE enumeration](..\wcndevice\ne-wcndevice-tagwcn_password_type.md) | WCN_PASSWORD_TYPE enumeration defines the authentication that will be used in a WPS session. |
| [tagWCN_SESSION_STATUS enumeration](..\wcndevice\ne-wcndevice-tagwcn_session_status.md) | Defines the outcome status of a WPS session. |
| [tagWCN_VALUE_TYPE_ASSOCIATION_STATE enumeration](..\wcntypes\ne-wcntypes-tagwcn_value_type_association_state.md) | WCN_VALUE_TYPE_ASSOCIATION_STATE enumeration defines the possible association states of a wireless station during a Discovery request. |
| [tagWCN_VALUE_TYPE_AUTHENTICATION_TYPE enumeration](..\wcntypes\ne-wcntypes-tagwcn_value_type_authentication_type.md) | WCN_VALUE_TYPE_AUTHENTICATION_TYPE enumeration defines the authentication types supported by the Enrollee (access point or station). |
| [tagWCN_VALUE_TYPE_BOOLEAN enumeration](..\wcntypes\ne-wcntypes-tagwcn_value_type_boolean.md) | WCN_VALUE_TYPE_BOOLEAN enumeration defines values used to represent true/false conditions encountered during device setup and association. |
| [tagWCN_VALUE_TYPE_CONFIGURATION_ERROR enumeration](..\wcntypes\ne-wcntypes-tagwcn_value_type_configuration_error.md) | WCN_VALUE_TYPE_CONFIGURATION_ERROR enumeration defines possible error values returned to a device while attempting to configure to, and associate with, the WLAN. |
| [tagWCN_VALUE_TYPE_CONFIG_METHODS enumeration](..\wcntypes\ne-wcntypes-tagwcn_value_type_config_methods.md) | WCN_VALUE_TYPE_CONFIG_METHODS enumeration defines the configuration methods supported by the Enrollee or Registrar. |
| [tagWCN_VALUE_TYPE_CONNECTION_TYPE enumeration](..\wcntypes\ne-wcntypes-tagwcn_value_type_connection_type.md) | WCN_VALUE_TYPE_CONNECTION_TYPE. |
| [tagWCN_VALUE_TYPE_DEVICE_PASSWORD_ID enumeration](..\wcntypes\ne-wcntypes-tagwcn_value_type_device_password_id.md) | WCN_VALUE_TYPE_DEVICE_PASSWORD_ID enumeration defines values that specify the origin or 'type' of a password. |
| [tagWCN_VALUE_TYPE_ENCRYPTION_TYPE enumeration](..\wcntypes\ne-wcntypes-tagwcn_value_type_encryption_type.md) | WCN_VALUE_TYPE_ENCRYPTION_TYPE enumeration defines the supported WLAN encryption types. |
| [tagWCN_VALUE_TYPE_RF_BANDS enumeration](..\wcntypes\ne-wcntypes-tagwcn_value_type_rf_bands.md) | WCN_VALUE_TYPE_RF_BANDS enumeration defines the possible radio frequency bands on which an enrollee can send Discovery requests. |
| [tagWCN_VALUE_TYPE_VERSION enumeration](..\wcntypes\ne-wcntypes-tagwcn_value_type_version.md) | Defines the supported version of Wi-Fi Protected Setup (WPS). |
| [tagWCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE enumeration](..\wcntypes\ne-wcntypes-tagwcn_value_type_wi_fi_protected_setup_state.md) | WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE enumeration. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IWCNConnectNotify interface](..\wcndevice\nn-wcndevice-iwcnconnectnotify.md) | Use this interface to receive a success or failure notification when a Windows Connect Now connect session completes. |
| [IWCNDevice interface](..\wcndevice\nn-wcndevice-iwcndevice.md) | Use this interface to configure the device and initiate the session. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IWCNConnectNotify::ConnectFailed](..\wcndevice\nf-wcndevice-iwcnconnectnotify-connectfailed.md) | Callback method indicates a IWCNDevice |
| [IWCNConnectNotify::ConnectSucceeded](..\wcndevice\nf-wcndevice-iwcnconnectnotify-connectsucceeded.md) | The IWCNConnectNotify |
| [IWCNDevice::Connect](..\wcndevice\nf-wcndevice-iwcndevice-connect.md) | The IWCNDevice |
| [IWCNDevice::GetAttribute](..\wcndevice\nf-wcndevice-iwcndevice-getattribute.md) | The IWCNDevice |
| [IWCNDevice::GetIntegerAttribute](..\wcndevice\nf-wcndevice-iwcndevice-getintegerattribute.md) | The GetIntegerAttribute method gets a cached attribute from the device as an integer. |
| [IWCNDevice::GetNetworkProfile](..\wcndevice\nf-wcndevice-iwcndevice-getnetworkprofile.md) | The IWCNDevice |
| [IWCNDevice::GetStringAttribute](..\wcndevice\nf-wcndevice-iwcndevice-getstringattribute.md) | The IWCNDevice |
| [IWCNDevice::GetVendorExtension](..\wcndevice\nf-wcndevice-iwcndevice-getvendorextension.md) | The GetVendorExtension method gets a cached vendor extension from the device. |
| [IWCNDevice::SetNetworkProfile](..\wcndevice\nf-wcndevice-iwcndevice-setnetworkprofile.md) | The IWCNDevice |
| [IWCNDevice::SetPassword](..\wcndevice\nf-wcndevice-iwcndevice-setpassword.md) | The IWCNDevice |
| [IWCNDevice::SetVendorExtension](..\wcndevice\nf-wcndevice-iwcndevice-setvendorextension.md) | The IWCNDevice |
| [IWCNDevice::Unadvise](..\wcndevice\nf-wcndevice-iwcndevice-unadvise.md) | IWCNDevice |
