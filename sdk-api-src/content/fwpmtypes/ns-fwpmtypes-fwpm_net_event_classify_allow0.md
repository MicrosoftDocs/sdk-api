---
UID: NS:fwpmtypes.FWPM_NET_EVENT_CLASSIFY_ALLOW0
title: FWPM_NET_EVENT_CLASSIFY_ALLOW0
author: windows-sdk-content
description: Contains information that describes allowed traffic as enforced by the WFP classify engine.
old-location: fwp\fwpm_net_event_classify_allow0.htm
old-project: FWP
ms.assetid: 4c7b665e-b248-4506-8d5f-bd27b05d8d50
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FWPM_NET_EVENT_CLASSIFY_ALLOW0, FWPM_NET_EVENT_CLASSIFY_ALLOW0 structure [Filtering], fwp.fwpm_net_event_classify_allow0, fwpmtypes/FWPM_NET_EVENT_CLASSIFY_ALLOW0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FWPM_NET_EVENT_CLASSIFY_ALLOW0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fwpmtypes.h
api_name:
-	FWPM_NET_EVENT_CLASSIFY_ALLOW0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
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
 

 

