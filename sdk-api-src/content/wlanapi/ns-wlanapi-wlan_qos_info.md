---
UID: NS:wlanapi._WLAN_QOS_INFO
title: WLAN_QOS_INFO
description: TBD
tech.root: nwifi
ms.date: 03/05/2024
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
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.typenames: WLAN_QOS_INFO, *PWLAN_QOS_INFO
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - _WLAN_QOS_INFO
 - PWLAN_QOS_INFO
 - WLAN_QOS_INFO
f1_keywords:
 - _WLAN_QOS_INFO
 - wlanapi/_WLAN_QOS_INFO
 - PWLAN_QOS_INFO
 - wlanapi/PWLAN_QOS_INFO
 - WLAN_QOS_INFO
 - wlanapi/WLAN_QOS_INFO
dev_langs:
 - c++
helpviewer_keywords:
 - _WLAN_QOS_INFO
prerelease: true
---

## -description

TBD

## -struct-fields

### -field interfaceCapabilities

Type: **[WLAN_QOS_CAPABILITIES](./ns-wlanapi-wlan_qos_capabilities.md)**

The QoS capabilities of the interface.

### -field ulConnectionQoSInfoSize

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

Indicates whether or not there's an established connection; and therefore whether the connection QoS info is present in connectionQoSInfo.

### -field ulConnectionQoSInfoOffset

Type: **[WLAN_CONNECTION_QOS_INFO](./ns-wlanapi-wlan_connection_qos_info.md)**

The QoS info of the current connection. Meaningful only if *bConnected* is `TRUE`; otherwise, *connectionQoSInfo* will be zeroed, and should be ignored.

## -remarks

## -see-also
