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

# _QOS_PACKET_PRIORITY structure


## -description


The <b>QOS_PACKET_PRIORITY</b> structure that indicates the priority of the flow traffic.


## -struct-fields




### -field ConformantDSCPValue

Differential Services Code Point (DSCP) mark used for flow traffic that conforms to the specified flow rate.


### -field NonConformantDSCPValue

DSCP marking used for flow traffic that exceeds the specified flow rate.  Non-conformant DSCP values are only applicable only if <a href="https://msdn.microsoft.com/8cd40e29-3af4-440c-8c44-3aeb5291e9c9">QOS_SHAPING</a> has a value of <b>QOSUseNonConformantMarkings</b>.


### -field ConformantL2Value

Layer-2 (L2) tag used for flow traffic that conforms to the specified flow rate. L2 tags will not be added to packets if the end-to-end path between source and sink does not support them.


### -field NonConformantL2Value

L2 tag used for flow traffic that exceeds the specified flow rate.  Non-conformant L2 values are only applicable if <a href="https://msdn.microsoft.com/8cd40e29-3af4-440c-8c44-3aeb5291e9c9">QOS_SHAPING</a> has a value of <b>QOSUseNonConformantMarkings</b>.


## -see-also




<a href="https://msdn.microsoft.com/8cae3ba2-beca-45e2-9526-2d917abc2606">QOSQueryFlow</a>



<a href="https://msdn.microsoft.com/022fde13-415e-49aa-8df4-472c4eadd6a0">Quality Windows Audio/Video Experience (qWAVE)</a>
 

 

