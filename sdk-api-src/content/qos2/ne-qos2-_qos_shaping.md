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

# _QOS_SHAPING enumeration


## -description


The <b>QOS_SHAPING</b> enumeration defines the shaping behavior of a flow.


## -enum-fields




### -field QOSShapeOnly

Indicates that the Windows packet scheduler (Pacer) will be used to enforce the requested flow rate. Data packets that exceed the rate are delayed until appropriate in order to maintain the specified flow rate.  If the network supports prioritization, packets will always receive conformant priority values when QOSShapeFlow is specified.


### -field QOSShapeAndMark

Indicates that the Windows Scheduler will be used to enforce the requested flow rate. Data packets exceeding the rate are delayed accordingly.  Packets receive conformant priority values.


### -field QOSUseNonConformantMarkings

Indicates that the flow rate requested will not be enforced.  Data packets that would exceed the flow rate will receive a priority that indicates they are non-conformant.  This may lead to lost and reordered packets.


## -see-also




<a href="https://msdn.microsoft.com/6f0408fa-842c-4c6c-954b-cdc8a77b4bd3">QOS_FLOWRATE_OUTGOING</a>



<a href="https://msdn.microsoft.com/022fde13-415e-49aa-8df4-472c4eadd6a0">Quality Windows Audio/Video Experience (qWAVE)</a>
 

 

