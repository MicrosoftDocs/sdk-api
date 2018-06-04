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

# CMSPCallMultiGraph::HandleGraphEvent


## -description


The 
<b>HandleGraphEvent</b> method is called by the 
<a href="https://msdn.microsoft.com/3f6f9145-1968-4067-936e-918f43ccbbcc">DispatchGraphEvent</a> static method to let the call object instance handle the event. It asks the filter graph for the event code and parameters, and queues an asynchronous work item on the global worker thread object, which will result in the <b>AsyncMultiGraphEvent</b> function (as defined in MSPCall.h) being executed on the worker thread. This is to allow the thread pool thread to return as quickly as possible, preventing an event storm from DirectShow's manual reset event.


## -parameters




### -param pContext

Contains pointer to 
<a href="https://msdn.microsoft.com/6a7fe6ea-8e25-469a-8505-55d48a661cd8">MSPSTREAMCONTEXT</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/86512d40-380b-4e98-840d-b7be99a86623">CMSPCallMultiGraph</a>
 

 

