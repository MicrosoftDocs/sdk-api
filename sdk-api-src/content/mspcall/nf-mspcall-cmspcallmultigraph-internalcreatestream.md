---
UID: NF:mspcall.CMSPCallMultiGraph.InternalCreateStream
title: CMSPCallMultiGraph::InternalCreateStream (mspcall.h)
description: The InternalCreateStream method is called by CreateStream to create a stream object (the caller does the argument checking).
helpviewer_keywords: ["CMSPCallMultiGraph interface [TAPI 2.2]","InternalCreateStream method","CMSPCallMultiGraph.InternalCreateStream","CMSPCallMultiGraph::InternalCreateStream","InternalCreateStream","InternalCreateStream method [TAPI 2.2]","InternalCreateStream method [TAPI 2.2]","CMSPCallMultiGraph interface","_tapi3_cmspcallmultigraph_internalcreatestream","mspcall/CMSPCallMultiGraph::InternalCreateStream","tapi3.cmspcallmultigraph_internalcreatestream"]
old-location: tapi3\cmspcallmultigraph_internalcreatestream.htm
tech.root: tapi3
ms.assetid: 62d098d5-b9cd-4e64-bec8-c4f736be22f9
ms.date: 12/05/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],InternalCreateStream method, CMSPCallMultiGraph.InternalCreateStream, CMSPCallMultiGraph::InternalCreateStream, InternalCreateStream, InternalCreateStream method [TAPI 2.2], InternalCreateStream method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_internalcreatestream, mspcall/CMSPCallMultiGraph::InternalCreateStream, tapi3.cmspcallmultigraph_internalcreatestream
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
 - CMSPCallMultiGraph::InternalCreateStream
 - mspcall/CMSPCallMultiGraph::InternalCreateStream
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
 - CMSPCallMultiGraph.InternalCreateStream
---

# CMSPCallMultiGraph::InternalCreateStream


## -description

The 
<b>InternalCreateStream</b> method is called by 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream">CreateStream</a> to create a stream object (the caller does the argument checking). It creates and initializes the stream object (using 
<a href="/windows/desktop/api/mspcall/nf-mspcall-cmspcallbase-createstreamobject">CreateStreamObject</a>). It uses <b>CoCreateInstance</b> to create a filter graph for the stream. It calls 
<a href="/windows/desktop/api/mspcall/nf-mspcall-cmspcallmultigraph-registerwaitevent">RegisterWaitEvent</a> to start waiting for events on the filter graph. It adds the stream into the call object's list of stream objects. It addrefs the stream pointer and returns it.

## -parameters

### -param dwMediaType

Descriptor of 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a> for stream.

### -param Direction

Descriptor of 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">terminal direction</a>.

### -param ppStream

Pointer to array of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interfaces.

## -see-also

<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallmultigraph">CMSPCallMultiGraph</a>