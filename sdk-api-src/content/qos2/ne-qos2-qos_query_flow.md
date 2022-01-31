---
UID: NE:qos2._QOS_QUERY_FLOW
title: QOS_QUERY_FLOW (qos2.h)
description: The QOS_QUERY_FLOW enumeration indicates the type of information a QOSQueryFlow function will request.
helpviewer_keywords: ["*PQOS_QUERY_FLOW","QOSQueryFlowFundamentals","QOSQueryOutgoingRate","QOSQueryPacketPriority","QOS_QUERY_FLOW","QOS_QUERY_FLOW enumeration [QOS]","qos.qos_query_flow","qos2/QOSQueryFlowFundamentals","qos2/QOSQueryOutgoingRate","qos2/QOSQueryPacketPriority","qos2/QOS_QUERY_FLOW"]
old-location: qos\qos_query_flow.htm
tech.root: QOS
ms.assetid: cae09751-0ac8-4fa1-9fdb-d2df3f01e504
ms.date: 12/05/2018
ms.keywords: '*PQOS_QUERY_FLOW, QOSQueryFlowFundamentals, QOSQueryOutgoingRate, QOSQueryPacketPriority, QOS_QUERY_FLOW, QOS_QUERY_FLOW enumeration [QOS], qos.qos_query_flow, qos2/QOSQueryFlowFundamentals, qos2/QOSQueryOutgoingRate, qos2/QOSQueryPacketPriority, qos2/QOS_QUERY_FLOW'
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
req.typenames: QOS_QUERY_FLOW, *PQOS_QUERY_FLOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_QUERY_FLOW
 - qos2/_QOS_QUERY_FLOW
 - PQOS_QUERY_FLOW
 - qos2/PQOS_QUERY_FLOW
 - QOS_QUERY_FLOW
 - qos2/QOS_QUERY_FLOW
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
 - QOS_QUERY_FLOW
---

# QOS_QUERY_FLOW enumeration


## -description

The <b>QOS_QUERY_FLOW</b> enumeration indicates the type of information a <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosqueryflow">QOSQueryFlow</a> function will request.

## -enum-fields

### -field QOSQueryFlowFundamentals:0

Indicates an information request for the flow fundamentals. This information includes bottleneck bandwidth, available bandwidth, and the average Round Trip Time (RTT)

### -field QOSQueryPacketPriority:1

Indicates a request for information detailing the QoS priority being added to flow packets.

### -field QOSQueryOutgoingRate:2

Indicates a request for the flow rate specified during the creation of an agreement with the QoS subsystem via the <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qossetflow">QOSSetFlow</a>  function.

## -see-also

<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosqueryflow">QOSQueryFlow</a>



<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>
