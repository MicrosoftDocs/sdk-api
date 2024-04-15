---
UID: NS:wlanapi._WLAN_QOS_CAPABILITIES
title: WLAN_QOS_CAPABILITIES
description: Contains capabilities of the features outlined in the WFA Wi-Fi QoS Management Specification.
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
req.typenames: WLAN_QOS_CAPABILITIES, *PWLAN_QOS_CAPABILITIES
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
 - _WLAN_QOS_CAPABILITIES
 - PWLAN_QOS_CAPABILITIES
 - WLAN_QOS_CAPABILITIES
f1_keywords:
 - _WLAN_QOS_CAPABILITIES
 - wlanapi/_WLAN_QOS_CAPABILITIES
 - PWLAN_QOS_CAPABILITIES
 - wlanapi/PWLAN_QOS_CAPABILITIES
 - WLAN_QOS_CAPABILITIES
 - wlanapi/WLAN_QOS_CAPABILITIES
dev_langs:
 - c++
helpviewer_keywords:
 - _WLAN_QOS_CAPABILITIES
prerelease: true
---

## -description

Contains capabilities of the features outlined in the [WFA Wi-Fi QoS Management Specification](https://www.wi-fi.org/news-events/newsroom/wi-fi-alliance-improves-quality-of-service-for-real-time-wi-fi-applications).

## -struct-fields

### -field bMSCSSupported

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

Represents whether Mirrored Stream Classification Service (MSCS) is supported.

### -field bDSCPToUPMappingSupported

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

Represents whether Differentiated Service Code Point (DSCP) to User Priority (UP) mapping is supported.

### -field bSCSSupported

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

Represents whether Stream Classification Service (SCS) is supported.

### -field bDSCPPolicySupported

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

Represents whether DSCP Policies are supported.

## -remarks

## -see-also
