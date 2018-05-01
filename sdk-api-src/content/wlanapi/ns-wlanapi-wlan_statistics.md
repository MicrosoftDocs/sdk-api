---
UID: NS:wlanapi.WLAN_STATISTICS
title: WLAN_STATISTICS
author: windows-driver-content
description: Assorted statistics about an interface.
old-location: nwifi\wlan_statistics.htm
old-project: NativeWiFi
ms.assetid: d66d89f1-bb12-4c2e-8c7a-a4eba008955d
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: "*PWLAN_STATISTICS, PWLAN_STATISTICS, PWLAN_STATISTICS structure pointer [NativeWIFI], WLAN_STATISTICS, WLAN_STATISTICS structure [NativeWIFI], nwifi.wlan_statistics, wlanapi/PWLAN_STATISTICS, wlanapi/WLAN_STATISTICS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: WLAN_STATISTICS, *PWLAN_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wlanapi.h
api_name:
-	WLAN_STATISTICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

A <a href="https://msdn.microsoft.com/b5bb4ec9-aeec-4a64-977d-e875c3835196">WLAN_MAC_FRAME_STATISTICS</a> structure that contains MAC layer counters for unicast packets directed to the receiver of the NIC.


### -field MacMcastCounters

A <a href="https://msdn.microsoft.com/b5bb4ec9-aeec-4a64-977d-e875c3835196">WLAN_MAC_FRAME_STATISTICS</a> structure that contains MAC layer counters for multicast packets directed to the current multicast address.


### -field dwNumberOfPhys

Contains the number of <b>WLAN_PHY_FRAME_STATISTICS</b> structures in the <b>PhyCounters</b> member.


### -field PhyCounters

An array of <a href="https://msdn.microsoft.com/c675a3cd-bbe5-473e-b734-12e74fd19a50">WLAN_PHY_FRAME_STATISTICS</a> structures that contain PHY layer counters.


## -see-also




<a href="https://msdn.microsoft.com/b5bb4ec9-aeec-4a64-977d-e875c3835196">WLAN_MAC_FRAME_STATISTICS</a>



<a href="https://msdn.microsoft.com/c675a3cd-bbe5-473e-b734-12e74fd19a50">WLAN_PHY_FRAME_STATISTICS</a>



<a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a>
 

 

