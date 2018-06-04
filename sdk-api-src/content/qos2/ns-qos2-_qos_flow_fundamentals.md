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

# _QOS_FLOW_FUNDAMENTALS structure


## -description


The <b>QOS_FLOW_FUNDAMENTALS</b> structure contains basic information about a flow.


## -struct-fields




### -field BottleneckBandwidthSet

This Boolean value is set to <b>TRUE</b> if the <b>BottleneckBandwidth</b> field contains a value.


### -field BottleneckBandwidth

Indicates the maximum end-to-end link capacity between the source and sink device, in bits.


### -field AvailableBandwidthSet

Set to <b>TRUE</b> if the <b>AvailableBandwidth</b> field contains a value.


### -field AvailableBandwidth

Indicates  how much bandwidth is available for submitting traffic on the end-to-end network path between the source and sink device, in bits.


### -field RTTSet

Set to <b>TRUE</b> if the <b>RTT</b> field contains a value.


### -field RTT

Measures the round-trip time between the source and sink device, in microseconds.


## -see-also




<a href="https://msdn.microsoft.com/8cae3ba2-beca-45e2-9526-2d917abc2606">QOSQueryFlow</a>



<a href="https://msdn.microsoft.com/022fde13-415e-49aa-8df4-472c4eadd6a0">Quality Windows Audio/Video Experience (qWAVE)</a>
 

 

