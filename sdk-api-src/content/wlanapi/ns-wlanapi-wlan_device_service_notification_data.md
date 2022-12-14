---
UID: NS:wlanapi._WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
title: WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
description: A structure that represents a device service notification.
tech.root: nwifi
helpviewer_keywords: ["_WLAN_DEVICE_SERVICE_NOTIFICATION_DATA"]
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
req.typenames: WLAN_DEVICE_SERVICE_NOTIFICATION_DATA, *PWLAN_DEVICE_SERVICE_NOTIFICATION_DATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - _WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
 - WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
f1_keywords:
 - _WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
 - wlanapi/_WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
 - PWLAN_DEVICE_SERVICE_NOTIFICATION_DATA
 - wlanapi/PWLAN_DEVICE_SERVICE_NOTIFICATION_DATA
 - WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
 - wlanapi/WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
dev_langs:
 - c++
---

## -description

A structure that represents a device service notification.

## -struct-fields

### -field DeviceService

Type: **[GUID](../guiddef/ns-guiddef-guid.md)**

The **GUID** identifying the device service for this notification.

### -field dwOpCode

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The opcode that identifies the operation under the device service for this notification.

### -field dwDataSize

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The size, in bytes, of the *DataBlob* member. The maximum value of *dwDataSize* may be restricted by the type of data that is stored in the **WLAN_DEVICE_SERVICE_NOTIFICATION_DATA** structure.

### -field DataBlob

Type: **[BYTE](../guiddef/ns-guiddef-guid.md)\[1\]**

A pointer to an array containing **BYTES**s, representing the data blob. This is the data that is received from the independent hardware vendor (IHV) driver, and is passed on to the client as an unformatted byte array blob.

## -remarks

## -see-also
