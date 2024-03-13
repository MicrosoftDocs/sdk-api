---
UID: NS:wlanapi._WLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO
title: WLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO
description: Contains information about a connected link.
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
req.target-type: 
req.typenames: WLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO, *PWLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO
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
 - _WLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO
 - PWLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO
 - WLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO
f1_keywords:
 - _WLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO
 - wlanapi/_WLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO
 - PWLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO
 - wlanapi/PWLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO
 - WLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO
 - wlanapi/WLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO
dev_langs:
 - c++
helpviewer_keywords:
 - _WLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO
prerelease: true
---

## -description

Contains information about a connected link.

## -struct-fields

### -field ucLinkID

The Link ID of the specific link.

### -field ulChannelCenterFrequencyMhz

The channel center frequency of the band on which the 802.11 Beacon or Probe Response frame was received. The value of *ulChannelCenterFrequencyMhz* is in units of kilohertz (kHz). 

> [!NOTE]
> This member is valid only for PHY types that are not frequency-hopping spread spectrum (FHSS).

### -field ulBandwidth

Bandwidth of the specific link.

### -field lRssi

The received signal strength indicator (RSSI) value, in units of decibels referenced to 1.0 milliwatts (dBm), as detected by the wireless LAN interface driver for the AP or peer station.

### -field wlanRateSet

A set of data transfer rates supported by the BSS. The data type for this member is a <a href="/windows/win32/api/wlanapi/ns-wlanapi-wlan_rate_set">WLAN_RATE_SET</a> structure.

## -remarks

## -see-also
