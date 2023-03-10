---
UID: NS:qos2._QOS_PACKET_PRIORITY
title: QOS_PACKET_PRIORITY (qos2.h)
description: The QOS_PACKET_PRIORITY structure that indicates the priority of the flow traffic.
helpviewer_keywords: ["*PQOS_PACKET_PRIORITY","PQOS_PACKET_PRIORITY","PQOS_PACKET_PRIORITY structure pointer [QOS]","QOS_PACKET_PRIORITY","QOS_PACKET_PRIORITY structure [QOS]","qos.qos_packet_priority","qos2/PQOS_PACKET_PRIORITY","qos2/QOS_PACKET_PRIORITY"]
old-location: qos\qos_packet_priority.htm
tech.root: QOS
ms.assetid: 1a10c5f0-0b7f-401f-82ff-0d7a93114715
ms.date: 12/05/2018
ms.keywords: '*PQOS_PACKET_PRIORITY, PQOS_PACKET_PRIORITY, PQOS_PACKET_PRIORITY structure pointer [QOS], QOS_PACKET_PRIORITY, QOS_PACKET_PRIORITY structure [QOS], qos.qos_packet_priority, qos2/PQOS_PACKET_PRIORITY, qos2/QOS_PACKET_PRIORITY'
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
req.typenames: QOS_PACKET_PRIORITY, *PQOS_PACKET_PRIORITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_PACKET_PRIORITY
 - qos2/_QOS_PACKET_PRIORITY
 - PQOS_PACKET_PRIORITY
 - qos2/PQOS_PACKET_PRIORITY
 - QOS_PACKET_PRIORITY
 - qos2/QOS_PACKET_PRIORITY
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
 - QOS_PACKET_PRIORITY
---

# QOS_PACKET_PRIORITY structure


## -description

The <b>QOS_PACKET_PRIORITY</b> structure that indicates the priority of the flow traffic.

## -struct-fields

### -field ConformantDSCPValue

Differential Services Code Point (DSCP) mark used for flow traffic that conforms to the specified flow rate.

### -field NonConformantDSCPValue

DSCP marking used for flow traffic that exceeds the specified flow rate.  Non-conformant DSCP values are only applicable only if <a href="/windows/desktop/api/qos2/ne-qos2-qos_shaping">QOS_SHAPING</a> has a value of <b>QOSUseNonConformantMarkings</b>.

### -field ConformantL2Value

Layer-2 (L2) tag used for flow traffic that conforms to the specified flow rate. L2 tags will not be added to packets if the end-to-end path between source and sink does not support them.

### -field NonConformantL2Value

L2 tag used for flow traffic that exceeds the specified flow rate.  Non-conformant L2 values are only applicable if <a href="/windows/desktop/api/qos2/ne-qos2-qos_shaping">QOS_SHAPING</a> has a value of <b>QOSUseNonConformantMarkings</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosqueryflow">QOSQueryFlow</a>



<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>