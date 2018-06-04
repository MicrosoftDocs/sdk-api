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

# CMSPCallMultiGraph::DispatchGraphEvent


## -description


The 
<b>DispatchGraphEvent</b> method is a static method posted to the 
<a href="https://msdn.microsoft.com/d0cd8b28-6e20-449a-94dd-cca2be46b812">RegisterWaitForSingleObject</a> function during initialization. This function is called when the filter graph signals the event. The <i>pContext</i> parameter is a pointer to the 
<a href="https://msdn.microsoft.com/6a7fe6ea-8e25-469a-8505-55d48a661cd8">MSPSTREAMCONTEXT</a> structure. The pointers in the structure carry ref counts. The implementation of this method simply casts the <i>pContext</i> argument to type MSPSTREAMCONTEXT *, and then calls 
<a href="https://msdn.microsoft.com/6c661341-6ae6-4a0a-88e5-b661a09ec9fe">HandleGraphEvent</a> on the MSP call object whose pointer appears in the structure.


## -parameters




### -param pContext

Contains pointer to 
<a href="https://msdn.microsoft.com/6a7fe6ea-8e25-469a-8505-55d48a661cd8">MSPSTREAMCONTEXT</a> structure.


### -param bFlag

Not used. Required for 
<a href="https://msdn.microsoft.com/d0cd8b28-6e20-449a-94dd-cca2be46b812">RegisterWaitForSingleObject</a>. Set <b>TRUE</b> if wait times out, but time-out in 
<a href="https://msdn.microsoft.com/3c75ed75-a0b2-435b-aa49-c1e7dadf260f">CMSPCallMultiGraph::RegisterWaitEvent</a> is set to INFINITE.


## -see-also




<a href="https://msdn.microsoft.com/86512d40-380b-4e98-840d-b7be99a86623">CMSPCallMultiGraph</a>
 

 

