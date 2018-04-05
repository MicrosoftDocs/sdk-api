---
UID: NS:qos2._QOS_FLOW_FUNDAMENTALS
title: "_QOS_FLOW_FUNDAMENTALS"
author: windows-driver-content
description: The QOS_FLOW_FUNDAMENTALS structure contains basic information about a flow.
old-location: qos\qos_flow_fundamentals.htm
old-project: QOS
ms.assetid: 3e6cbd5b-8bd3-4f08-9192-35604db5dc3a
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*PQOS_FLOW_FUNDAMENTALS, PQOS_FLOW_FUNDAMENTALS, PQOS_FLOW_FUNDAMENTALS structure pointer [QOS], QOS_FLOW_FUNDAMENTALS, QOS_FLOW_FUNDAMENTALS structure [QOS], _QOS_FLOW_FUNDAMENTALS, qos.qos_flow_fundamentals, qos2/PQOS_FLOW_FUNDAMENTALS, qos2/QOS_FLOW_FUNDAMENTALS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: qos2.h
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
req.typenames: QOS_FLOW_FUNDAMENTALS, *PQOS_FLOW_FUNDAMENTALS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Qos2.h
api_name:
-	QOS_FLOW_FUNDAMENTALS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
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
 

 

