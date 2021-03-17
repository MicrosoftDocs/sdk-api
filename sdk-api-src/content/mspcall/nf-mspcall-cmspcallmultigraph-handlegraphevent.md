---
UID: NF:mspcall.CMSPCallMultiGraph.HandleGraphEvent
title: CMSPCallMultiGraph::HandleGraphEvent (mspcall.h)
description: The HandleGraphEvent method is called by the DispatchGraphEvent static method to let the call object instance handle the event.
helpviewer_keywords: ["CMSPCallMultiGraph interface [TAPI 2.2]","HandleGraphEvent method","CMSPCallMultiGraph.HandleGraphEvent","CMSPCallMultiGraph::HandleGraphEvent","HandleGraphEvent","HandleGraphEvent method [TAPI 2.2]","HandleGraphEvent method [TAPI 2.2]","CMSPCallMultiGraph interface","_tapi3_cmspcallmultigraph_handlegraphevent","mspcall/CMSPCallMultiGraph::HandleGraphEvent","tapi3.cmspcallmultigraph_handlegraphevent"]
old-location: tapi3\cmspcallmultigraph_handlegraphevent.htm
tech.root: tapi3
ms.assetid: 6c661341-6ae6-4a0a-88e5-b661a09ec9fe
ms.date: 12/05/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],HandleGraphEvent method, CMSPCallMultiGraph.HandleGraphEvent, CMSPCallMultiGraph::HandleGraphEvent, HandleGraphEvent, HandleGraphEvent method [TAPI 2.2], HandleGraphEvent method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_handlegraphevent, mspcall/CMSPCallMultiGraph::HandleGraphEvent, tapi3.cmspcallmultigraph_handlegraphevent
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CMSPCallMultiGraph::HandleGraphEvent
 - mspcall/CMSPCallMultiGraph::HandleGraphEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspcall.h
api_name:
 - CMSPCallMultiGraph.HandleGraphEvent
---

# CMSPCallMultiGraph::HandleGraphEvent


## -description

The 
<b>HandleGraphEvent</b> method is called by the 
<a href="/windows/desktop/api/mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent">DispatchGraphEvent</a> static method to let the call object instance handle the event. It asks the filter graph for the event code and parameters, and queues an asynchronous work item on the global worker thread object, which will result in the <b>AsyncMultiGraphEvent</b> function (as defined in MSPCall.h) being executed on the worker thread. This is to allow the thread pool thread to return as quickly as possible, preventing an event storm from DirectShow's manual reset event.

## -parameters

### -param pContext

Contains pointer to 
<a href="/previous-versions/windows/desktop/legacy/ms733448(v=vs.85)">MSPSTREAMCONTEXT</a> structure.

## -see-also

<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallmultigraph">CMSPCallMultiGraph</a>