---
UID: NS:wlanapi._WLAN_CONNECTION_QOS_INFO
title: WLAN_CONNECTION_QOS_INFO
description: Contains information about the QoS features outlined by the WFA Wi-Fi QoS Management Specification pertaining to the current connection.
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
req.typenames: WLAN_CONNECTION_QOS_INFO, *PWLAN_CONNECTION_QOS_INFO
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
 - _WLAN_CONNECTION_QOS_INFO
 - PWLAN_CONNECTION_QOS_INFO
 - WLAN_CONNECTION_QOS_INFO
f1_keywords:
 - _WLAN_CONNECTION_QOS_INFO
 - wlanapi/_WLAN_CONNECTION_QOS_INFO
 - PWLAN_CONNECTION_QOS_INFO
 - wlanapi/PWLAN_CONNECTION_QOS_INFO
 - WLAN_CONNECTION_QOS_INFO
 - wlanapi/WLAN_CONNECTION_QOS_INFO
dev_langs:
 - c++
helpviewer_keywords:
 - _WLAN_CONNECTION_QOS_INFO
prerelease: true
---

## -description

Contains information about the QoS features outlined by the [WFA Wi-Fi QoS Management Specification](https://www.wi-fi.org/news-events/newsroom/wi-fi-alliance-improves-quality-of-service-for-real-time-wi-fi-applications) pertaining to the current connection.

## -struct-fields

### -field peerCapabilities

Type: **[WLAN_QOS_CAPABILITIES](./ns-wlanapi-wlan_qos_capabilities.md)**

The QoS capabilities of the current peer.

### -field bMSCSConfigured

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

Represents whether Mirrored Stream Classification Service (MSCS) is enabled on the current connection.

### -field bDSCPToUPMappingConfigured

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

Represents whether Differentiated Service Code Point (DSCP) to User Priority (UP) mapping is enabled on the current connection.

### -field ulNumConfiguredSCSStreams

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

Represents the number of Stream Classification Service (SCS) streams configured on the current connection.

### -field ulNumConfiguredDSCPPolicies

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

Represents the number of DSCP Policies configured on the current connection.

## -remarks

## -see-also
