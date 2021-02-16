---
UID: NS:qos2._QOS_FLOW_FUNDAMENTALS
title: QOS_FLOW_FUNDAMENTALS (qos2.h)
description: The QOS_FLOW_FUNDAMENTALS structure contains basic information about a flow.
helpviewer_keywords: ["*PQOS_FLOW_FUNDAMENTALS","PQOS_FLOW_FUNDAMENTALS","PQOS_FLOW_FUNDAMENTALS structure pointer [QOS]","QOS_FLOW_FUNDAMENTALS","QOS_FLOW_FUNDAMENTALS structure [QOS]","qos.qos_flow_fundamentals","qos2/PQOS_FLOW_FUNDAMENTALS","qos2/QOS_FLOW_FUNDAMENTALS"]
old-location: qos\qos_flow_fundamentals.htm
tech.root: QOS
ms.assetid: 3e6cbd5b-8bd3-4f08-9192-35604db5dc3a
ms.date: 12/05/2018
ms.keywords: '*PQOS_FLOW_FUNDAMENTALS, PQOS_FLOW_FUNDAMENTALS, PQOS_FLOW_FUNDAMENTALS structure pointer [QOS], QOS_FLOW_FUNDAMENTALS, QOS_FLOW_FUNDAMENTALS structure [QOS], qos.qos_flow_fundamentals, qos2/PQOS_FLOW_FUNDAMENTALS, qos2/QOS_FLOW_FUNDAMENTALS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: QOS_FLOW_FUNDAMENTALS, *PQOS_FLOW_FUNDAMENTALS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_FLOW_FUNDAMENTALS
 - qos2/_QOS_FLOW_FUNDAMENTALS
 - PQOS_FLOW_FUNDAMENTALS
 - qos2/PQOS_FLOW_FUNDAMENTALS
 - QOS_FLOW_FUNDAMENTALS
 - qos2/QOS_FLOW_FUNDAMENTALS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qos2.h
api_name:
 - QOS_FLOW_FUNDAMENTALS
---

# QOS_FLOW_FUNDAMENTALS structure


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

<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosqueryflow">QOSQueryFlow</a>



<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>