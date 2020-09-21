---
UID: NS:qos2._QOS_FLOWRATE_OUTGOING
title: QOS_FLOWRATE_OUTGOING (qos2.h)
description: The QOS_FLOWRATE_OUTGOING structure is used to set flow rate information in the QOSSetFlow function.
helpviewer_keywords: ["*PQOS_FLOWRATE_OUTGOING","PQOS_FLOWRATE_OUTGOING","PQOS_FLOWRATE_OUTGOING structure pointer [QOS]","QOS_FLOWRATE_OUTGOING","QOS_FLOWRATE_OUTGOING structure [QOS]","qos.qos_flowrate_outgoing","qos2/PQOS_FLOWRATE_OUTGOING","qos2/QOS_FLOWRATE_OUTGOING"]
old-location: qos\qos_flowrate_outgoing.htm
tech.root: QOS
ms.assetid: 6f0408fa-842c-4c6c-954b-cdc8a77b4bd3
ms.date: 12/05/2018
ms.keywords: '*PQOS_FLOWRATE_OUTGOING, PQOS_FLOWRATE_OUTGOING, PQOS_FLOWRATE_OUTGOING structure pointer [QOS], QOS_FLOWRATE_OUTGOING, QOS_FLOWRATE_OUTGOING structure [QOS], qos.qos_flowrate_outgoing, qos2/PQOS_FLOWRATE_OUTGOING, qos2/QOS_FLOWRATE_OUTGOING'
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
req.typenames: QOS_FLOWRATE_OUTGOING, *PQOS_FLOWRATE_OUTGOING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_FLOWRATE_OUTGOING
 - qos2/_QOS_FLOWRATE_OUTGOING
 - PQOS_FLOWRATE_OUTGOING
 - qos2/PQOS_FLOWRATE_OUTGOING
 - QOS_FLOWRATE_OUTGOING
 - qos2/QOS_FLOWRATE_OUTGOING
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
 - QOS_FLOWRATE_OUTGOING
---

# QOS_FLOWRATE_OUTGOING structure


## -description

The <b>QOS_FLOWRATE_OUTGOING</b> structure is used to set flow rate information in the <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qossetflow">QOSSetFlow</a> function.

## -struct-fields

### -field Bandwidth

The rate at which data should be sent, in units of bits per second.

<div class="alert"><b>Note</b>  Traffic on the network is measured at the IP level, and not at the application level.  The rate that is specified should account for the IP and protocol headers.</div>
<div> </div>

### -field ShapingBehavior

A <a href="/windows/desktop/api/qos2/ne-qos2-qos_shaping">QOS_SHAPING</a> constant that defines the shaping behavior of the flow.

### -field Reason

A <a href="/windows/desktop/api/qos2/ne-qos2-qos_flowrate_reason">QOS_FLOWRATE_REASON</a> constant that indicates the reason for a flow rate change.

## -see-also

<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qossetflow">QOSSetFlow</a>



<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>