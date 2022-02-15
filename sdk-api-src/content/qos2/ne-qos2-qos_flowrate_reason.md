---
UID: NE:qos2._QOS_FLOWRATE_REASON
title: QOS_FLOWRATE_REASON (qos2.h)
description: The QOS_FLOWRATE_REASON enumeration indicates the reason for a change in a flow's bandwidth.
helpviewer_keywords: ["*PQOS_FLOWRATE_REASON","PQOS_FLOWRATE_REASON","PQOS_FLOWRATE_REASON enumeration [QOS]","QOSFlowRateCongestion","QOSFlowRateContentChange","QOSFlowRateHigherContentEncoding","QOSFlowRateNotApplicable","QOSFlowRateUserCaused","QOS_FLOWRATE_REASON","QOS_FLOWRATE_REASON enumeration [QOS]","qos.qos_flowrate_reason","qos2/PQOS_FLOWRATE_REASON","qos2/QOSFlowRateCongestion","qos2/QOSFlowRateContentChange","qos2/QOSFlowRateHigherContentEncoding","qos2/QOSFlowRateNotApplicable","qos2/QOSFlowRateUserCaused","qos2/QOS_FLOWRATE_REASON"]
old-location: qos\qos_flowrate_reason.htm
tech.root: QOS
ms.assetid: bd2a1fec-d554-49e2-8803-624942455f74
ms.date: 12/05/2018
ms.keywords: '*PQOS_FLOWRATE_REASON, PQOS_FLOWRATE_REASON, PQOS_FLOWRATE_REASON enumeration [QOS], QOSFlowRateCongestion, QOSFlowRateContentChange, QOSFlowRateHigherContentEncoding, QOSFlowRateNotApplicable, QOSFlowRateUserCaused, QOS_FLOWRATE_REASON, QOS_FLOWRATE_REASON enumeration [QOS], qos.qos_flowrate_reason, qos2/PQOS_FLOWRATE_REASON, qos2/QOSFlowRateCongestion, qos2/QOSFlowRateContentChange, qos2/QOSFlowRateHigherContentEncoding, qos2/QOSFlowRateNotApplicable, qos2/QOSFlowRateUserCaused, qos2/QOS_FLOWRATE_REASON'
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
req.typenames: QOS_FLOWRATE_REASON, *PQOS_FLOWRATE_REASON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_FLOWRATE_REASON
 - qos2/_QOS_FLOWRATE_REASON
 - PQOS_FLOWRATE_REASON
 - qos2/PQOS_FLOWRATE_REASON
 - QOS_FLOWRATE_REASON
 - qos2/QOS_FLOWRATE_REASON
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
 - QOS_FLOWRATE_REASON
---

# QOS_FLOWRATE_REASON enumeration


## -description

The <b>QOS_FLOWRATE_REASON</b> enumeration indicates the reason for a change in a flow's bandwidth.

## -enum-fields

### -field QOSFlowRateNotApplicable:0

Indicates that there has not been a change in the flow.

### -field QOSFlowRateContentChange:1

Indicates that the content of a flow has changed.

### -field QOSFlowRateCongestion:2

Indicates that the flow has changed due to congestion.

### -field QOSFlowRateHigherContentEncoding:3

### -field QOSFlowRateUserCaused:4

Indicates that the user has caused the flow to change.

## -see-also

<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosqueryflow">QOSQueryFlow</a>



<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>
