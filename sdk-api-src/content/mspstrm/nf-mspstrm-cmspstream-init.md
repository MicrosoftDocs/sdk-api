---
UID: NF:mspstrm.CMSPStream.Init
title: CMSPStream::Init
author: windows-sdk-content
description: The Init method is called by the MSPCall when the stream is created. It initializes the members, calls MSPCallAddRef on the call object, and queries for various interfaces on the filter graph.
old-location: tapi3\cmspstream_init.htm
tech.root: Tapi
ms.assetid: 8e522987-ac94-4597-8491-4c66b15aa262
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CMSPStream interface [TAPI 2.2],Init method, CMSPStream.Init, CMSPStream::Init, Init, Init method [TAPI 2.2], Init method [TAPI 2.2],CMSPStream interface, _tapi3_cmspstream_init, mspstrm/CMSPStream::Init, tapi3.cmspstream_init
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMSPStream::Init


## -description


The 
<b>Init</b> method is called by the <b>MSPCall</b> when the stream is created. It initializes the members, calls 
<a href="https://msdn.microsoft.com/fe70ceac-660e-4fdd-960f-b61503bc8939">MSPCallAddRef</a> on the call object, and queries for various interfaces on the filter graph.


## -parameters




### -param hAddress

Handle for address associated with this call.


### -param pMSPCall

Pointer to MSP basic calling handler class, 
<a href="https://msdn.microsoft.com/77b53b66-38fa-4823-9051-e857da8a7dd7">CMSPCallBase</a>.


### -param pGraph

Pointer to <b>IMediaEvent</b> interface for the stream's filter graph. This DirectShow interface supports event notification to the application from the filter graph and from filters within the filter graph.


### -param dwMediaType

Descriptor of 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a> for stream.


### -param Direction

Descriptor of 
<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">terminal direction</a>.


## -see-also




<a href="https://msdn.microsoft.com/776ca663-faa2-4534-8873-4e20ed79530c">CMSPStream</a>
 

 

