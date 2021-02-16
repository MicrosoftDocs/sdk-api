---
UID: NF:mspcall.CMSPCallMultiGraph.ProcessGraphEvent
title: CMSPCallMultiGraph::ProcessGraphEvent (mspcall.h)
description: The ProcessGraphEvent method (as defined in MSPCall.h) is called on the MSP worker thread.
helpviewer_keywords: ["CMSPCallMultiGraph interface [TAPI 2.2]","ProcessGraphEvent method","CMSPCallMultiGraph.ProcessGraphEvent","CMSPCallMultiGraph::ProcessGraphEvent","ProcessGraphEvent","ProcessGraphEvent method [TAPI 2.2]","ProcessGraphEvent method [TAPI 2.2]","CMSPCallMultiGraph interface","_tapi3_cmspcallmultigraph_processgraphevent","mspcall/CMSPCallMultiGraph::ProcessGraphEvent","tapi3.cmspcallmultigraph_processgraphevent"]
old-location: tapi3\cmspcallmultigraph_processgraphevent.htm
tech.root: tapi3
ms.assetid: 2b41a8ac-8aa1-47d0-ad90-f6f177895149
ms.date: 12/05/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],ProcessGraphEvent method, CMSPCallMultiGraph.ProcessGraphEvent, CMSPCallMultiGraph::ProcessGraphEvent, ProcessGraphEvent, ProcessGraphEvent method [TAPI 2.2], ProcessGraphEvent method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_processgraphevent, mspcall/CMSPCallMultiGraph::ProcessGraphEvent, tapi3.cmspcallmultigraph_processgraphevent
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
 - CMSPCallMultiGraph::ProcessGraphEvent
 - mspcall/CMSPCallMultiGraph::ProcessGraphEvent
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
 - CMSPCallMultiGraph.ProcessGraphEvent
---

# CMSPCallMultiGraph::ProcessGraphEvent


## -description

The <b>ProcessGraphEvent</b> method (as defined in MSPCall.h) is called on the MSP worker thread. It calls this method to let the call object instance handle the event, and then releases the call object and stream object references in its context structure. This method finds the indicated stream and dispatches the call to the 
<b>ProcessGraphEvent</b> method on the appropriate Stream object.

## -parameters

### -param pITStream

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface.

### -param lEventCode

Filled in by filter graph. Implementation dependent.

### -param lParam1

Filled in by filter graph. Implementation dependent.

### -param lParam2

Filled in by filter graph. Implementation dependent.

## -see-also

<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallmultigraph">CMSPCallMultiGraph</a>