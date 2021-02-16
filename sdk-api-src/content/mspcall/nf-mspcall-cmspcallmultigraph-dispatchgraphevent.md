---
UID: NF:mspcall.CMSPCallMultiGraph.DispatchGraphEvent
title: CMSPCallMultiGraph::DispatchGraphEvent (mspcall.h)
description: The DispatchGraphEvent method is a static method posted to the RegisterWaitForSingleObject function during initialization.
helpviewer_keywords: ["CMSPCallMultiGraph interface [TAPI 2.2]","DispatchGraphEvent method","CMSPCallMultiGraph.DispatchGraphEvent","CMSPCallMultiGraph::DispatchGraphEvent","DispatchGraphEvent","DispatchGraphEvent method [TAPI 2.2]","DispatchGraphEvent method [TAPI 2.2]","CMSPCallMultiGraph interface","_tapi3_cmspcallmultigraph_dispatchgraphevent","mspcall/CMSPCallMultiGraph::DispatchGraphEvent","tapi3.cmspcallmultigraph_dispatchgraphevent"]
old-location: tapi3\cmspcallmultigraph_dispatchgraphevent.htm
tech.root: tapi3
ms.assetid: 3f6f9145-1968-4067-936e-918f43ccbbcc
ms.date: 12/05/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],DispatchGraphEvent method, CMSPCallMultiGraph.DispatchGraphEvent, CMSPCallMultiGraph::DispatchGraphEvent, DispatchGraphEvent, DispatchGraphEvent method [TAPI 2.2], DispatchGraphEvent method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_dispatchgraphevent, mspcall/CMSPCallMultiGraph::DispatchGraphEvent, tapi3.cmspcallmultigraph_dispatchgraphevent
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
 - CMSPCallMultiGraph::DispatchGraphEvent
 - mspcall/CMSPCallMultiGraph::DispatchGraphEvent
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
 - CMSPCallMultiGraph.DispatchGraphEvent
---

# CMSPCallMultiGraph::DispatchGraphEvent


## -description

The 
<b>DispatchGraphEvent</b> method is a static method posted to the 
<a href="/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject">RegisterWaitForSingleObject</a> function during initialization. This function is called when the filter graph signals the event. The <i>pContext</i> parameter is a pointer to the 
<a href="/previous-versions/windows/desktop/legacy/ms733448(v=vs.85)">MSPSTREAMCONTEXT</a> structure. The pointers in the structure carry ref counts. The implementation of this method simply casts the <i>pContext</i> argument to type MSPSTREAMCONTEXT *, and then calls 
<a href="/windows/desktop/api/mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent">HandleGraphEvent</a> on the MSP call object whose pointer appears in the structure.

## -parameters

### -param pContext

Contains pointer to 
<a href="/previous-versions/windows/desktop/legacy/ms733448(v=vs.85)">MSPSTREAMCONTEXT</a> structure.

### -param bFlag

Not used. Required for 
<a href="/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject">RegisterWaitForSingleObject</a>. Set <b>TRUE</b> if wait times out, but time-out in 
<a href="/windows/desktop/api/mspcall/nf-mspcall-cmspcallmultigraph-registerwaitevent">CMSPCallMultiGraph::RegisterWaitEvent</a> is set to INFINITE.

## -see-also

<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallmultigraph">CMSPCallMultiGraph</a>