---
UID: NF:mspcall.CMSPCallMultiGraph.HandleGraphEvent
title: CMSPCallMultiGraph::HandleGraphEvent method
author: windows-driver-content
description: The HandleGraphEvent method is called by the DispatchGraphEvent static method to let the call object instance handle the event.
old-location: tapi3\cmspcallmultigraph_handlegraphevent.htm
old-project: Tapi
ms.assetid: 6c661341-6ae6-4a0a-88e5-b661a09ec9fe
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: CMSPCallMultiGraph, CMSPCallMultiGraph interface [TAPI 2.2], HandleGraphEvent method, CMSPCallMultiGraph::HandleGraphEvent, HandleGraphEvent method [TAPI 2.2], HandleGraphEvent method [TAPI 2.2], CMSPCallMultiGraph interface, HandleGraphEvent,CMSPCallMultiGraph.HandleGraphEvent, _tapi3_cmspcallmultigraph_handlegraphevent, mspcall/CMSPCallMultiGraph::HandleGraphEvent, tapi3.cmspcallmultigraph_handlegraphevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mspcall.h
req.include-header: 
req.target-type: Windows
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
req.typenames: MSPEVENTITEM, *PMSPEVENTITEM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mspcall.h
api_name:
-	CMSPCallMultiGraph.HandleGraphEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CMSPCallMultiGraph::HandleGraphEvent method


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
 

 

