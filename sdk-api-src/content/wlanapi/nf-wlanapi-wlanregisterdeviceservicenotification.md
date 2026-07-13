---
UID: NF:wlanapi.WlanRegisterDeviceServiceNotification
title: WlanRegisterDeviceServiceNotification
description: Allows user mode clients with admin privileges, or User-Mode Driver Framework (UMDF) drivers, to register for unsolicited notifications corresponding to device services that they're interested in.
tech.root: nwifi
helpviewer_keywords: ["WlanRegisterDeviceServiceNotification"]
ms.date: 12/18/2019
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wlanapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: OneCoreUAP.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - wlanapi.dll
api_name:
 - WlanRegisterDeviceServiceNotification
f1_keywords:
 - WlanRegisterDeviceServiceNotification
 - wlanapi/WlanRegisterDeviceServiceNotification
dev_langs:
 - c++
---

## -description

Allows user mode clients with admin privileges, or User-Mode Driver Framework (UMDF) drivers, to register for unsolicited notifications corresponding to device services that they're interested in.

## -parameters

### -param hClientHandle

Type: **[HANDLE](/windows/win32/winprog/windows-data-types)**

The client's session handle, obtained by a previous call to the [WlanOpenHandle](./nf-wlanapi-wlanopenhandle.md) function.

### -param pDevSvcGuidList

Type: **CONST [PWLAN_DEVICE_SERVICE_GUID_LIST](./ns-wlanapi-wlan_device_service_guid_list.md)**

An optional pointer to a constant [WLAN_DEVICE_SERVICE_GUID_LIST](./ns-wlanapi-wlan_device_service_guid_list.md) structure representing the device service **GUID**s for which you're interested in receiving notifications. The *dwIndex* member of the structure must have a value less than the value of its *dwNumberOfItems* member; otherwise, an access violation may occur. Every time you call this API, the previous device services list is replaced by the new one.

To unregister, set *pDevSvcGuidList* to `nullptr`, or pass a pointer to a **WLAN_DEVICE_SERVICE_GUID_LIST** structure that has the `dwNumberOfItems` member set to 0.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, the return value is **ERROR_SUCCESS**. If the function fails with **ERROR_ACCESS_DENIED**, then the caller doesn't have sufficient permissions to perform this operation. The caller needs to either have admin privilege, or needs to be a UMDF driver.

## -remarks

The **WlanRegisterDeviceServiceNotification** function is an extension to existing native Wi-Fi APIs for WLAN device services.

A client application calls this function to register and unregister notifications for device services that it is interested in.

Any registration to receive notifications for device services caused by this function would be automatically undone if the calling application closes its calling handle (by calling [WlanCloseHandle](./nf-wlanapi-wlanclosehandle.md) with the *hClientHandle* parameter), or if the process ends.

In order to receive these notifications, a client needs to call this function with a valid *pDevSvcGuidList* parameter, and must also call the [WlanRegisterNotification](./nf-wlanapi-wlanregisternotification.md) function with a *dwNotifSource* argument of **WLAN_NOTIFICATION_SOURCE_DEVICE_SERVICE** (which is defined in `wlanapi.h`). The registration to receive notifications for device services is in effect until the application closes the client handle (by calling [WlanCloseHandle](./nf-wlanapi-wlanclosehandle.md) with the *hClientHandle* parameter), or the process ends, or **WlanRegisterDeviceServiceNotification** is called with a *pDevSvcGuidList* argument of `nullptr`, or else has *dwNumberOfItems* set to 0.

When the operating system (OS) receives a device service notification from an independent hardware vendor (IHV) driver, and a client has registered for these notifications using **WlanRegisterDeviceServiceNotification**, the client will receive them via the [WLAN_NOTIFICATION_CALLBACK](./nc-wlanapi-wlan_notification_callback.md) that it had registered through its call to [WlanRegisterNotification](./nf-wlanapi-wlanregisternotification.md). This callback will be called for every notification that the client has received (with a separate buffer for every notification).

The *NotificationSource* member of the [WLAN_NOTIFICATION_DATA](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) structure received by the callback function (that is, the *data* member) will be set to **WLAN_NOTIFICATION_SOURCE_DEVICE_SERVICE**. The data blob, the device service **GUID**, and the opcode associated with this notification will be present in the *pData* member of the **WLAN_NOTIFICATION_DATA**, which will point to a structure of type [WLAN_DEVICE_SERVICE_NOTIFICATION_DATA](./ns-wlanapi-wlan_device_service_notification_data.md).

> [!NOTE]
> The WLAN service, or the OS, will not check to see whether the device service **GUID**s that the client registers for are actually supported by the IHV driver. It is up to the client to query for supported device services using [WlanGetSupportedDeviceServices](./nf-wlanapi-wlangetsupporteddeviceservices.md) API if they need to.

## -see-also
