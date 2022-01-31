---
UID: NE:qos2._QOS_SHAPING
title: QOS_SHAPING (qos2.h)
description: The QOS_SHAPING enumeration defines the shaping behavior of a flow.
helpviewer_keywords: ["*PQOS_SHAPING","PQOS_SHAPING","PQOS_SHAPING enumeration pointer [QOS]","QOSShapeAndMark","QOSShapeOnly","QOSUseNonConformantMarkings","QOS_SHAPING","QOS_SHAPING enumeration [QOS]","qos.qos_shaping","qos2/PQOS_SHAPING","qos2/QOSShapeAndMark","qos2/QOSShapeOnly","qos2/QOSUseNonConformantMarkings","qos2/QOS_SHAPING"]
old-location: qos\qos_shaping.htm
tech.root: QOS
ms.assetid: 8cd40e29-3af4-440c-8c44-3aeb5291e9c9
ms.date: 12/05/2018
ms.keywords: '*PQOS_SHAPING, PQOS_SHAPING, PQOS_SHAPING enumeration pointer [QOS], QOSShapeAndMark, QOSShapeOnly, QOSUseNonConformantMarkings, QOS_SHAPING, QOS_SHAPING enumeration [QOS], qos.qos_shaping, qos2/PQOS_SHAPING, qos2/QOSShapeAndMark, qos2/QOSShapeOnly, qos2/QOSUseNonConformantMarkings, qos2/QOS_SHAPING'
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
req.typenames: QOS_SHAPING, *PQOS_SHAPING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_SHAPING
 - qos2/_QOS_SHAPING
 - PQOS_SHAPING
 - qos2/PQOS_SHAPING
 - QOS_SHAPING
 - qos2/QOS_SHAPING
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
 - QOS_SHAPING
---

# QOS_SHAPING enumeration


## -description

The <b>QOS_SHAPING</b> enumeration defines the shaping behavior of a flow.

## -enum-fields

### -field QOSShapeOnly:0

Indicates that the Windows packet scheduler (Pacer) will be used to enforce the requested flow rate. Data packets that exceed the rate are delayed until appropriate in order to maintain the specified flow rate.  If the network supports prioritization, packets will always receive conformant priority values when QOSShapeFlow is specified.

### -field QOSShapeAndMark:1

Indicates that the Windows Scheduler will be used to enforce the requested flow rate. Data packets exceeding the rate are delayed accordingly.  Packets receive conformant priority values.

### -field QOSUseNonConformantMarkings:2

Indicates that the flow rate requested will not be enforced.  Data packets that would exceed the flow rate will receive a priority that indicates they are non-conformant.  This may lead to lost and reordered packets.

## -see-also

<a href="/windows/desktop/api/qos2/ns-qos2-qos_flowrate_outgoing">QOS_FLOWRATE_OUTGOING</a>



<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>
