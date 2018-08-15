---
UID: NF:mspcall.CMSPCallBase.InternalCreateStream
title: CMSPCallBase::InternalCreateStream
author: windows-sdk-content
description: The InternalCreateStream method is called by CreateStream to create a stream object (the caller does the argument checking). It should create and initialize the stream object (using CreateStreamObject).
old-location: tapi3\cmspcallbase_internalcreatestream.htm
old-project: tapi
ms.assetid: 6f9cef2e-36dd-4095-9060-b6d37ccbc6d7
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],InternalCreateStream method, CMSPCallBase.InternalCreateStream, CMSPCallBase::InternalCreateStream, InternalCreateStream, InternalCreateStream method [TAPI 2.2], InternalCreateStream method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_internalcreatestream, mspcall/CMSPCallBase::InternalCreateStream, tapi3.cmspcallbase_internalcreatestream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mspcall.h
req.include-header: 
req.redist: 
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
 - CMSPCallBase.InternalCreateStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CMSPCallBase::InternalCreateStream


## -description


The 
<b>InternalCreateStream</b> method is called by 
<a href="https://msdn.microsoft.com/402cde43-6b2a-4e4e-bf46-97fcafb7574a">CreateStream</a> to create a stream object (the caller does the argument checking). It should create and initialize the stream object (using 
<a href="https://msdn.microsoft.com/ac98dd08-4250-40f6-91a8-e1f67b94b51f">CreateStreamObject</a>).


## -parameters




### -param dwMediaType


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media type</a> or types of call.


### -param Direction

Indicates 
<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">terminal direction</a>.


### -param ppStream

Pointer to 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> object interface.


## -see-also




<a href="https://msdn.microsoft.com/77b53b66-38fa-4823-9051-e857da8a7dd7">CMSPCallBase</a>



<a href="https://msdn.microsoft.com/62d098d5-b9cd-4e64-bec8-c4f736be22f9">CMSPCallMultiGraph::InternalCreateStream</a>



<a href="https://msdn.microsoft.com/402cde43-6b2a-4e4e-bf46-97fcafb7574a">CreateStream</a>



<a href="https://msdn.microsoft.com/ac98dd08-4250-40f6-91a8-e1f67b94b51f">CreateStreamObject</a>



<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>
 

 

