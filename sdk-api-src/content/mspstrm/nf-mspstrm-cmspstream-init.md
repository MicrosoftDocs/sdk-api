---
UID: NF:mspstrm.CMSPStream.Init
title: CMSPStream::Init (mspstrm.h)
description: The Init method is called by the MSPCall when the stream is created. It initializes the members, calls MSPCallAddRef on the call object, and queries for various interfaces on the filter graph.helpviewer_keywords: ["CMSPStream interface [TAPI 2.2]","Init method","CMSPStream.Init","CMSPStream::Init","Init","Init method [TAPI 2.2]","Init method [TAPI 2.2]","CMSPStream interface","_tapi3_cmspstream_init","mspstrm/CMSPStream::Init","tapi3.cmspstream_init"]
old-location: tapi3\cmspstream_init.htm
tech.root: Tapi
ms.assetid: 8e522987-ac94-4597-8491-4c66b15aa262
ms.date: 12/05/2018
ms.keywords: CMSPStream interface [TAPI 2.2],Init method, CMSPStream.Init, CMSPStream::Init, Init, Init method [TAPI 2.2], Init method [TAPI 2.2],CMSPStream interface, _tapi3_cmspstream_init, mspstrm/CMSPStream::Init, tapi3.cmspstream_init
f1_keywords:
- mspstrm/CMSPStream.Init
dev_langs:
- c++
req.header: mspstrm.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mspstrm.h
api_name:
- CMSPStream.Init
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CMSPStream::Init


## -description


The 
<b>Init</b> method is called by the <b>MSPCall</b> when the stream is created. It initializes the members, calls 
<a href="https://docs.microsoft.com/windows/desktop/api/mspcall/nf-mspcall-cmspcallbase-mspcalladdref">MSPCallAddRef</a> on the call object, and queries for various interfaces on the filter graph.


## -parameters




### -param hAddress

Handle for address associated with this call.


### -param pMSPCall

Pointer to MSP basic calling handler class, 
<a href="https://docs.microsoft.com/windows/desktop/api/mspcall/nl-mspcall-cmspcallbase">CMSPCallBase</a>.


### -param pGraph

Pointer to <b>IMediaEvent</b> interface for the stream's filter graph. This DirectShow interface supports event notification to the application from the filter graph and from filters within the filter graph.


### -param dwMediaType

Descriptor of 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapimediatype--constants">media type</a> for stream.


### -param Direction

Descriptor of 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">terminal direction</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mspstrm/nl-mspstrm-cmspstream">CMSPStream</a>
 

 

