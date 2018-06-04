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

# FWPM_NET_EVENT_CLASSIFY_ALLOW0 structure


## -description


The <b>FWPM_NET_EVENT_CLASSIFY_ALLOW0</b> structure contains information that describes allowed traffic as enforced by the WFP classify engine.


## -struct-fields




### -field filterId

Type: <b>UINT64</b>

A LUID identifying the WFP filter allowing this traffic.


### -field layerId

Type: <b>UINT16</b>

The identifier of the WFP filtering layer where the filter specified  in <b>filterId</b> is stored. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff549947">Filtering Layer Identifiers</a>.


### -field reauthReason

Type: <b>UINT32</b>

The reason for reauthorizing a previously authorized connection.


### -field originalProfile

Type: <b>UINT32</b>

The identifier of the profile to which the packet was received (or from which the packet was sent).


### -field currentProfile

Type: <b>UINT32</b>

The identifier of the profile where the packet was when the failure occurred.


### -field msFwpDirection

Type: <b>UINT32</b>

Indicates the direction of the packet transmission. Possible values are <b>FWP_DIRECTION_INBOUND</b> or <b>FWP_DIRECTION_OUTBOUND</b>.


### -field isLoopback

Type: <b>BOOL</b>

If true, indicates that the packet originated from (or was heading to) the loopback adapter; otherwise, false. 


## -see-also




<a href="https://msdn.microsoft.com/fbcacfb1-b471-474e-bdee-12a481fadc63">FWPM_NET_EVENT2</a>
 

 

