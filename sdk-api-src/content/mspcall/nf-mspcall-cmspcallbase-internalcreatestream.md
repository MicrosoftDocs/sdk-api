---
UID: NF:mspcall.CMSPCallBase.InternalCreateStream
title: CMSPCallBase::InternalCreateStream (mspcall.h)
author: windows-sdk-content
description: The InternalCreateStream method is called by CreateStream to create a stream object (the caller does the argument checking). It should create and initialize the stream object (using CreateStreamObject).
old-location: tapi3\cmspcallbase_internalcreatestream.htm
tech.root: Tapi
ms.assetid: 6f9cef2e-36dd-4095-9060-b6d37ccbc6d7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],InternalCreateStream method, CMSPCallBase.InternalCreateStream, CMSPCallBase::InternalCreateStream, InternalCreateStream, InternalCreateStream method [TAPI 2.2], InternalCreateStream method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_internalcreatestream, mspcall/CMSPCallBase::InternalCreateStream, tapi3.cmspcallbase_internalcreatestream
ms.topic: method
f1_keywords: ["mspcall/CMSPCallBase.InternalCreateStream"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspcall.h
api_name:
 - CMSPCallBase.InternalCreateStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CMSPCallBase::InternalCreateStream


## -description


The 
<b>InternalCreateStream</b> method is called by 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream">CreateStream</a> to create a stream object (the caller does the argument checking). It should create and initialize the stream object (using 
<a href="https://docs.microsoft.com/windows/desktop/api/mspcall/nf-mspcall-cmspcallbase-createstreamobject">CreateStreamObject</a>).


## -parameters




### -param dwMediaType


<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapimediatype--constants">Media type</a> or types of call.


### -param Direction

Indicates 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">terminal direction</a>.


### -param ppStream

Pointer to 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> object interface.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mspcall/nl-mspcall-cmspcallbase">CMSPCallBase</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mspcall/nf-mspcall-cmspcallmultigraph-internalcreatestream">CMSPCallMultiGraph::InternalCreateStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream">CreateStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mspcall/nf-mspcall-cmspcallbase-createstreamobject">CreateStreamObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>
 

 

