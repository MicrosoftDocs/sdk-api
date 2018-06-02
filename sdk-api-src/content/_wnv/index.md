---
UID: TP:wnv
ms.assetid: 0373728d-f3cc-3b01-ab7e-474698d5e450
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# Windows Network Virtualization



Overview of the Windows Network Virtualization technology.

To develop Windows Network Virtualization, you need these headers:

 * [wnvapi.h](..\wnvapi\index.md)

For the programming guide, see [Windows Network Virtualization](/previous-versions/windows/desktop/wnv).

## Functions

| Title   | Description   |
| ---- |:---- |
| [WnvOpen function](..\wnvapi\nf-wnvapi-wnvopen.md) | Provides a handle to the Windows Network Virtualization (WNV) driver object to be used to request and receive WNV notifications. |
| [WnvRequestNotification function](..\wnvapi\nf-wnvapi-wnvrequestnotification.md) | Requests notification from the Windows Network Virtualization (WNV) driver whenever a certain type of event occurs. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_WNV_IP_ADDRESS structure](..\wnvapi\ns-wnvapi-_wnv_ip_address.md) | Defines an IP address object. |
| [_WNV_NOTIFICATION_PARAM structure](..\wnvapi\ns-wnvapi-_wnv_notification_param.md) | Specifies the version, notification type, and the buffer location in a WnvRequestNotification function call. |
| [_WNV_OBJECT_CHANGE_PARAM structure](..\wnvapi\ns-wnvapi-_wnv_object_change_param.md) | Specifies the parameters of an event that causes the Windows Network Virtualization (WNV) driver to generate a WnvObjectChangeType type of notification. |
| [_WNV_OBJECT_HEADER structure](..\wnvapi\ns-wnvapi-_wnv_object_header.md) | Specifies the major version, minor version, and buffer size of the WNV_NOTIFICATION_PARAM structure that is passed to the WnvRequestNotification function. |
| [_WNV_POLICY_MISMATCH_PARAM structure](..\wnvapi\ns-wnvapi-_wnv_policy_mismatch_param.md) | Specifies the parameters of an event (typically an incoming packet) that causes the Windows Network Virtualization (WNV) driver to generate a WnvPolicyMismatchType notification. |
| [_WNV_PROVIDER_ADDRESS_CHANGE_PARAM structure](..\wnvapi\ns-wnvapi-_wnv_provider_address_change_param.md) | Specifies the provider address's DAD (duplicate address detection) status change, which causes the Windows Network Virtualization (WNV) driver to generate a WnvObjectChangeType notification that specifies the WnvProviderAddressType object type containing this structure. |
| [_WNV_REDIRECT_PARAM structure](..\wnvapi\ns-wnvapi-_wnv_redirect_param.md) | Specifies the parameters of the event (receiving an incoming Internet Control Message Protocol redirect packet) that causes the Windows Network Virtualization (WNV) driver to generate a WnvRedirectType notification. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [_WNV_NOTIFICATION_TYPE enumeration](..\wnvapi\ne-wnvapi-_wnv_notification_type.md) | Specifies the type of a given Windows Network Virtualization (WNV) notification. |
| [_WNV_OBJECT_TYPE enumeration](..\wnvapi\ne-wnvapi-_wnv_object_type.md) | Specifies the object type of a given Windows Network Virtualization (WNV) notification when the WNV notification type is WnvObjectChangeType. |
