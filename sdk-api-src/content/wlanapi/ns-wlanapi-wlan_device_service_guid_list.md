---
UID: NS:wlanapi._WLAN_DEVICE_SERVICE_GUID_LIST
title: WLAN_DEVICE_SERVICE_GUID_LIST
description: Contains an array of device service GUIDs.
tech.root: nwifi
helpviewer_keywords: ["_WLAN_DEVICE_SERVICE_GUID_LIST"]
ms.date: 12/18/2019
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: wlanapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: WLAN_DEVICE_SERVICE_GUID_LIST, *PWLAN_DEVICE_SERVICE_GUID_LIST
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - _WLAN_DEVICE_SERVICE_GUID_LIST
 - WLAN_DEVICE_SERVICE_GUID_LIST
f1_keywords:
 - _WLAN_DEVICE_SERVICE_GUID_LIST
 - wlanapi/_WLAN_DEVICE_SERVICE_GUID_LIST
 - PWLAN_DEVICE_SERVICE_GUID_LIST
 - wlanapi/PWLAN_DEVICE_SERVICE_GUID_LIST
 - WLAN_DEVICE_SERVICE_GUID_LIST
 - wlanapi/WLAN_DEVICE_SERVICE_GUID_LIST
dev_langs:
 - c++
---

## -description

Contains an array of device service GUIDs.

## -struct-fields

### -field dwNumberOfItems

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The number of items in the *DeviceService* argument.

### -field dwIndex

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The index of the current item. The index of the first item is 0. *dwIndex* must be less than *dwNumberOfItems*. This member is not used by the wireless service. You can use this member when processing individual **GUID**s in the **WLAN_DEVICE_SERVICE_GUID_LIST** structure. When your application passes this structure from one function to another, it can set the value of *dwIndex* to the index of the item currently being processed. This can help your application maintain state. You should always initialize *dwIndex* before use.

### -field DeviceService

Type: **[GUID](../guiddef/ns-guiddef-guid.md)\[1\]**

A pointer to an array containing **GUID**s; each corresponds to a WLAN device service that the driver supports.

## -remarks

## -see-also
