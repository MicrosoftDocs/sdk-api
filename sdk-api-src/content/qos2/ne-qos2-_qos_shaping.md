---
UID: NE:qos2._QOS_SHAPING
title: "_QOS_SHAPING"
author: windows-sdk-content
description: The QOS_SHAPING enumeration defines the shaping behavior of a flow.
old-location: qos\qos_shaping.htm
old-project: QOS
ms.assetid: 8cd40e29-3af4-440c-8c44-3aeb5291e9c9
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: "*PQOS_SHAPING, PQOS_SHAPING, PQOS_SHAPING enumeration pointer [QOS], QOSShapeAndMark, QOSShapeOnly, QOSUseNonConformantMarkings, QOS_SHAPING, QOS_SHAPING enumeration [QOS], _QOS_SHAPING, qos.qos_shaping, qos2/PQOS_SHAPING, qos2/QOSShapeAndMark, qos2/QOSShapeOnly, qos2/QOSUseNonConformantMarkings, qos2/QOS_SHAPING"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: QOS_SHAPING, *PQOS_SHAPING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qos2.h
api_name:
 - QOS_SHAPING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

