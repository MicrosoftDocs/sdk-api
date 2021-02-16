---
UID: NS:wlanapi.WLAN_STATISTICS
title: WLAN_STATISTICS (wlanapi.h)
description: Assorted statistics about an interface.
helpviewer_keywords: ["*PWLAN_STATISTICS","PWLAN_STATISTICS","PWLAN_STATISTICS structure pointer [NativeWIFI]","WLAN_STATISTICS","WLAN_STATISTICS structure [NativeWIFI]","nwifi.wlan_statistics","wlanapi/PWLAN_STATISTICS","wlanapi/WLAN_STATISTICS"]
old-location: nwifi\wlan_statistics.htm
tech.root: nwifi
ms.assetid: d66d89f1-bb12-4c2e-8c7a-a4eba008955d
ms.date: 12/05/2018
ms.keywords: '*PWLAN_STATISTICS, PWLAN_STATISTICS, PWLAN_STATISTICS structure pointer [NativeWIFI], WLAN_STATISTICS, WLAN_STATISTICS structure [NativeWIFI], nwifi.wlan_statistics, wlanapi/PWLAN_STATISTICS, wlanapi/WLAN_STATISTICS'
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WLAN_STATISTICS, *PWLAN_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WLAN_STATISTICS
 - wlanapi/WLAN_STATISTICS
 - PWLAN_STATISTICS
 - wlanapi/PWLAN_STATISTICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_STATISTICS
---

# WLAN_STATISTICS structure


## -description

The <b>WLAN_STATISTICS</b> structure contains assorted statistics about an interface.

## -struct-fields

### -field ullFourWayHandshakeFailures

Indicates the number of 4-way handshake failures.  This member is only valid if IHV Service is being used as the authentication service for the current network.

### -field ullTKIPCounterMeasuresInvoked

Indicates the number of TKIP countermeasures performed by an IHV Miniport driver.  This count does not include TKIP countermeasures invoked by the operating system.

### -field ullReserved

Reserved for use by Microsoft.

### -field MacUcastCounters

A <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_mac_frame_statistics">WLAN_MAC_FRAME_STATISTICS</a> structure that contains MAC layer counters for unicast packets directed to the receiver of the NIC.

### -field MacMcastCounters

A <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_mac_frame_statistics">WLAN_MAC_FRAME_STATISTICS</a> structure that contains MAC layer counters for multicast packets directed to the current multicast address.

### -field dwNumberOfPhys

Contains the number of <b>WLAN_PHY_FRAME_STATISTICS</b> structures in the <b>PhyCounters</b> member.

### -field PhyCounters.unique

### -field PhyCounters.size_is

### -field PhyCounters.size_is.dwNumberOfPhys

### -field PhyCounters

An array of <a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_phy_frame_statistics">WLAN_PHY_FRAME_STATISTICS</a> structures that contain PHY layer counters.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_mac_frame_statistics">WLAN_MAC_FRAME_STATISTICS</a>



<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_phy_frame_statistics">WLAN_PHY_FRAME_STATISTICS</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a>