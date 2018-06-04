---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


### -field PhyCounters.unique

 


### -field PhyCounters.size_is

 


### -field PhyCounters.size_is.dwNumberOfPhys

 


### -field PhyCounters

An array of <a href="https://msdn.microsoft.com/c675a3cd-bbe5-473e-b734-12e74fd19a50">WLAN_PHY_FRAME_STATISTICS</a> structures that contain PHY layer counters.


## -see-also




<a href="https://msdn.microsoft.com/b5bb4ec9-aeec-4a64-977d-e875c3835196">WLAN_MAC_FRAME_STATISTICS</a>



<a href="https://msdn.microsoft.com/c675a3cd-bbe5-473e-b734-12e74fd19a50">WLAN_PHY_FRAME_STATISTICS</a>



<a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a>
 

 

