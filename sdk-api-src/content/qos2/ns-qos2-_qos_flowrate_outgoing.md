---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

