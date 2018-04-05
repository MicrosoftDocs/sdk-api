---
UID: NS:qos2._QOS_FLOWRATE_OUTGOING
title: "_QOS_FLOWRATE_OUTGOING"
author: windows-driver-content
description: The QOS_FLOWRATE_OUTGOING structure is used to set flow rate information in the QOSSetFlow function.
old-location: qos\qos_flowrate_outgoing.htm
old-project: QOS
ms.assetid: 6f0408fa-842c-4c6c-954b-cdc8a77b4bd3
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*PQOS_FLOWRATE_OUTGOING, PQOS_FLOWRATE_OUTGOING, PQOS_FLOWRATE_OUTGOING structure pointer [QOS], QOS_FLOWRATE_OUTGOING, QOS_FLOWRATE_OUTGOING structure [QOS], _QOS_FLOWRATE_OUTGOING, qos.qos_flowrate_outgoing, qos2/PQOS_FLOWRATE_OUTGOING, qos2/QOS_FLOWRATE_OUTGOING"
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
req.typenames: QOS_FLOWRATE_OUTGOING, *PQOS_FLOWRATE_OUTGOING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Qos2.h
api_name:
-	QOS_FLOWRATE_OUTGOING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _QOS_FLOWRATE_OUTGOING structure


## -description


The <b>QOS_FLOWRATE_OUTGOING</b> structure is used to set flow rate information in the <a href="https://msdn.microsoft.com/b30e8887-4445-480d-aba8-79ec36384648">QOSSetFlow</a> function.


## -struct-fields




### -field Bandwidth

The rate at which data should be sent, in units of bits per second.

<div class="alert"><b>Note</b>  Traffic on the network is measured at the IP level, and not at the application level.  The rate that is specified should account for the IP and protocol headers.</div>
<div> </div>

### -field ShapingBehavior

A <a href="https://msdn.microsoft.com/8cd40e29-3af4-440c-8c44-3aeb5291e9c9">QOS_SHAPING</a> constant that defines the shaping behavior of the flow.


### -field Reason

A <a href="https://msdn.microsoft.com/bd2a1fec-d554-49e2-8803-624942455f74">QOS_FLOWRATE_REASON</a> constant that indicates the reason for a flow rate change.


## -see-also




<a href="https://msdn.microsoft.com/b30e8887-4445-480d-aba8-79ec36384648">QOSSetFlow</a>



<a href="https://msdn.microsoft.com/022fde13-415e-49aa-8df4-472c4eadd6a0">Quality Windows Audio/Video Experience (qWAVE)</a>
 

 

