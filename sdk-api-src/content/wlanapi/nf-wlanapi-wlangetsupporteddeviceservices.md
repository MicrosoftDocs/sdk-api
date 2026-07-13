---
UID: NF:wlanapi.WlanGetSupportedDeviceServices
title: WlanGetSupportedDeviceServices
description: Retrieves a list of the supported device services on a given wireless LAN interface.
tech.root: nwifi
helpviewer_keywords: ["WlanGetSupportedDeviceServices"]
ms.date: 01/07/2019
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
 - WlanGetSupportedDeviceServices
f1_keywords:
 - WlanGetSupportedDeviceServices
 - wlanapi/WlanGetSupportedDeviceServices
dev_langs:
 - c++
---

## -description

Retrieves a list of the supported device services on a given wireless LAN interface.

## -parameters

### -param hClientHandle [in]

Type: **[HANDLE](/windows/win32/winprog/windows-data-types)**

The client's session handle, obtained by a previous call to the [WlanOpenHandle](./nf-wlanapi-wlanopenhandle.md) function.

### -param pInterfaceGuid [in]

Type: **CONST [GUID](../guiddef/ns-guiddef-guid.md)\***

A pointer to the **GUID** of the wireless LAN interface to be queried. You can determine the **GUID** of each wireless LAN interface enabled on a local computer by using the [WlanEnumInterfaces](./nf-wlanapi-wlanenuminterfaces.md) function.

### -param ppDevSvcGuidList [out]

Type: **[PWLAN_DEVICE_SERVICE_GUID_LIST](./ns-wlanapi-wlan_device_service_guid_list.md)\***

A pointer to storage for a pointer to receive the returned list of device service **GUID**s in a [WLAN_DEVICE_SERVICE_GUID_LIST](./ns-wlanapi-wlan_device_service_guid_list.md) structure. If the call succeeds, then the buffer for the **WLAN_DEVICE_SERVICE_GUID_LIST** returned is allocated by the **WlanGetSupportedDeviceServices** function.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, the return value is **ERROR_SUCCESS**. If the function fails with **ERROR_ACCESS_DENIED**, then the caller doesn't have sufficient permissions to perform this operation. The caller needs to either have admin privilege, or needs to be a UMDF driver.

## -remarks

If the call succeeds, then the **WlanGetSupportedDeviceServices** function allocates memory for the device services **GUID** list that's returned in a buffer pointed to by the *ppDevSvcGuidList* parameter. When you no longer need the buffer pointed to by *ppDevSvcGuidList*, you should release the memory used for it by calling the [WlanFreeMemory](./nf-wlanapi-wlanfreememory.md) function.

## -see-also
