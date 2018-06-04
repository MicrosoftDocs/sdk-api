---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# CMSPCallMultiGraph::InternalCreateStream


## -description


The 
<b>InternalCreateStream</b> method is called by 
<a href="https://msdn.microsoft.com/402cde43-6b2a-4e4e-bf46-97fcafb7574a">CreateStream</a> to create a stream object (the caller does the argument checking). It creates and initializes the stream object (using 
<a href="https://msdn.microsoft.com/ac98dd08-4250-40f6-91a8-e1f67b94b51f">CreateStreamObject</a>). It uses <b>CoCreateInstance</b> to create a filter graph for the stream. It calls 
<a href="https://msdn.microsoft.com/3c75ed75-a0b2-435b-aa49-c1e7dadf260f">RegisterWaitEvent</a> to start waiting for events on the filter graph. It adds the stream into the call object's list of stream objects. It addrefs the stream pointer and returns it.


## -parameters




### -param dwMediaType

Descriptor of 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a> for stream.


### -param Direction

Descriptor of 
<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">terminal direction</a>.


### -param ppStream

Pointer to array of 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interfaces.


## -see-also




<a href="https://msdn.microsoft.com/86512d40-380b-4e98-840d-b7be99a86623">CMSPCallMultiGraph</a>
 

 

