---
UID: NF:mspcall.CMSPCallMultiGraph.RemoveStream
title: CMSPCallMultiGraph::RemoveStream (mspcall.h)
description: (Interface RemoveStream) The RemoveStream method is called by the application to remove a stream from the call. (CMSPCallMultiGraph.RemoveStream)
helpviewer_keywords: ["CMSPCallMultiGraph interface [TAPI 2.2]","RemoveStream method","CMSPCallMultiGraph.RemoveStream","CMSPCallMultiGraph::RemoveStream","RemoveStream","RemoveStream method [TAPI 2.2]","RemoveStream method [TAPI 2.2]","CMSPCallMultiGraph interface","_tapi3_cmspcallmultigraph_removestream","mspcall/CMSPCallMultiGraph::RemoveStream","tapi3.cmspcallmultigraph_removestream"]
old-location: tapi3\cmspcallmultigraph_removestream.htm
tech.root: tapi3
ms.assetid: 03572d9a-f243-4423-b645-ef180704477f
ms.date: 12/05/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],RemoveStream method, CMSPCallMultiGraph.RemoveStream, CMSPCallMultiGraph::RemoveStream, RemoveStream, RemoveStream method [TAPI 2.2], RemoveStream method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_removestream, mspcall/CMSPCallMultiGraph::RemoveStream, tapi3.cmspcallmultigraph_removestream
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
 - CMSPCallMultiGraph::RemoveStream
 - mspcall/CMSPCallMultiGraph::RemoveStream
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
 - CMSPCallMultiGraph.RemoveStream
---

# CMSPCallMultiGraph::RemoveStream


## -description

(Interface 
<b>RemoveStream</b>) The 
<b>RemoveStream</b> method is called by the application to remove a stream from the call. Derived MSP call objects that do not want to allow applications to remove streams should override this to simply return TAPI_E_NOTSUPPORTED. (This is a good simplification strategy for many MSPs.) The default implementation removes the stream object from the call object's list of streams and releases the call's references to the stream.

## -parameters

### -param ppStream

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface for stream to be removed from the call.

## -see-also

<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallmultigraph">CMSPCallMultiGraph</a>
