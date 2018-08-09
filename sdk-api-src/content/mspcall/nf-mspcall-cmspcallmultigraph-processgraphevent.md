---
UID: NF:mspcall.CMSPCallMultiGraph.ProcessGraphEvent
title: CMSPCallMultiGraph::ProcessGraphEvent
author: windows-sdk-content
description: The ProcessGraphEvent method (as defined in MSPCall.h) is called on the MSP worker thread.
old-location: tapi3\cmspcallmultigraph_processgraphevent.htm
old-project: tapi
ms.assetid: 2b41a8ac-8aa1-47d0-ad90-f6f177895149
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],ProcessGraphEvent method, CMSPCallMultiGraph.ProcessGraphEvent, CMSPCallMultiGraph::ProcessGraphEvent, ProcessGraphEvent, ProcessGraphEvent method [TAPI 2.2], ProcessGraphEvent method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_processgraphevent, mspcall/CMSPCallMultiGraph::ProcessGraphEvent, tapi3.cmspcallmultigraph_processgraphevent
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSPEVENTITEM, *PMSPEVENTITEM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspcall.h
api_name:
 - CMSPCallMultiGraph.ProcessGraphEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CMSPCallMultiGraph::ProcessGraphEvent


## -description


The <b>ProcessGraphEvent</b> method (as defined in MSPCall.h) is called on the MSP worker thread. It calls this method to let the call object instance handle the event, and then releases the call object and stream object references in its context structure. This method finds the indicated stream and dispatches the call to the 
<b>ProcessGraphEvent</b> method on the appropriate Stream object.


## -parameters




### -param pITStream

Pointer to 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface.


### -param lEventCode

Filled in by filter graph. Implementation dependent.


### -param lParam1

Filled in by filter graph. Implementation dependent.


### -param lParam2

Filled in by filter graph. Implementation dependent.


## -see-also




<a href="https://msdn.microsoft.com/86512d40-380b-4e98-840d-b7be99a86623">CMSPCallMultiGraph</a>
 

 

