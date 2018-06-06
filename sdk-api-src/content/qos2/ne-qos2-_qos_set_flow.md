---
UID: NE:qos2._QOS_SET_FLOW
title: "_QOS_SET_FLOW"
author: windows-sdk-content
description: The QOS_SET_FLOW enumeration indicates what is being changed about a flow.
old-location: qos\qos_set_flow.htm
old-project: QOS
ms.assetid: 986652bc-df2f-4210-bf9c-1a5d8c3ee773
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: "*PQOS_SET_FLOW, PQOS_SET_FLOW, PQOS_SET_FLOW enumeration pointer [QOS], QOSSetOutgoingDSCPValue, QOSSetOutgoingRate, QOSSetTrafficType, QOS_SET_FLOW, QOS_SET_FLOW enumeration [QOS], _QOS_SET_FLOW, qos.qos_set_flow, qos2/PQOS_SET_FLOW, qos2/QOSSetOutgoingDSCPValue, qos2/QOSSetOutgoingRate, qos2/QOSSetTrafficType, qos2/QOS_SET_FLOW"
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
req.typenames: QOS_SET_FLOW, *PQOS_SET_FLOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qos2.h
api_name:
 - QOS_SET_FLOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _QOS_SET_FLOW enumeration


## -description


The <b>QOS_SET_FLOW</b> enumeration indicates what is being changed about a flow.


## -enum-fields




### -field QOSSetTrafficType

Indicates that the traffic type of the flow will change.


### -field QOSSetOutgoingRate

Indicates that the flow rate will change.


### -field QOSSetOutgoingDSCPValue

Windows 7, Windows Server 2008 R2, and later: Indicates that the outgoing DSCP value will change.

<div class="alert"><b>Note</b>  This setting requires the calling application be a member of the Administrators or the  Network Configuration Operators group.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/b30e8887-4445-480d-aba8-79ec36384648">QOSSetFlow</a>



<a href="https://msdn.microsoft.com/022fde13-415e-49aa-8df4-472c4eadd6a0">Quality Windows Audio/Video Experience (qWAVE)</a>
 

 

