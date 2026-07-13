---
UID: NE:qos2._QOS_SET_FLOW
title: QOS_SET_FLOW (qos2.h)
description: The QOS_SET_FLOW enumeration indicates what is being changed about a flow.
helpviewer_keywords: ["*PQOS_SET_FLOW","PQOS_SET_FLOW","PQOS_SET_FLOW enumeration pointer [QOS]","QOSSetOutgoingDSCPValue","QOSSetOutgoingRate","QOSSetTrafficType","QOS_SET_FLOW","QOS_SET_FLOW enumeration [QOS]","qos.qos_set_flow","qos2/PQOS_SET_FLOW","qos2/QOSSetOutgoingDSCPValue","qos2/QOSSetOutgoingRate","qos2/QOSSetTrafficType","qos2/QOS_SET_FLOW"]
old-location: qos\qos_set_flow.htm
tech.root: QOS
ms.assetid: 986652bc-df2f-4210-bf9c-1a5d8c3ee773
ms.date: 12/05/2018
ms.keywords: '*PQOS_SET_FLOW, PQOS_SET_FLOW, PQOS_SET_FLOW enumeration pointer [QOS], QOSSetOutgoingDSCPValue, QOSSetOutgoingRate, QOSSetTrafficType, QOS_SET_FLOW, QOS_SET_FLOW enumeration [QOS], qos.qos_set_flow, qos2/PQOS_SET_FLOW, qos2/QOSSetOutgoingDSCPValue, qos2/QOSSetOutgoingRate, qos2/QOSSetTrafficType, qos2/QOS_SET_FLOW'
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
req.typenames: QOS_SET_FLOW, *PQOS_SET_FLOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_SET_FLOW
 - qos2/_QOS_SET_FLOW
 - PQOS_SET_FLOW
 - qos2/PQOS_SET_FLOW
 - QOS_SET_FLOW
 - qos2/QOS_SET_FLOW
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
 - QOS_SET_FLOW
---

# QOS_SET_FLOW enumeration


## -description

The <b>QOS_SET_FLOW</b> enumeration indicates what is being changed about a flow.

## -enum-fields

### -field QOSSetTrafficType:0

Indicates that the traffic type of the flow will change.

### -field QOSSetOutgoingRate:1

Indicates that the flow rate will change.

### -field QOSSetOutgoingDSCPValue:2

Windows 7, Windows Server 2008 R2, and later: Indicates that the outgoing DSCP value will change.

<div class="alert"><b>Note</b>  This setting requires the calling application be a member of the Administrators or the  Network Configuration Operators group.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qossetflow">QOSSetFlow</a>



<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>
