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

# CMSPCallBase::CreateStreamObject


## -description


The 
<b>CreateStreamObject</b> method is called by 
<a href="https://msdn.microsoft.com/6f9cef2e-36dd-4095-9060-b6d37ccbc6d7">InternalCreateStream</a>. The derived class should <b>CreateInstance</b> on its stream object, do an ATL <b>_InternalQueryInterface</b> to obtain an 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> pointer from the stream object, and call the stream object's 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a> method (on the stream object pointer, not the 
<b>ITStream</b> pointer).


## -parameters




### -param dwMediaType


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media type</a> of stream to be created.


### -param Direction


<a href="https://msdn.microsoft.com/library/windows/hardware/ff547596">Direction</a> of stream.


### -param pGraph

Pointer to DirectShow <b>IMediaEvent</b> interface.


### -param ppStream

Pointer to 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface.


## -see-also




<a href="https://msdn.microsoft.com/77b53b66-38fa-4823-9051-e857da8a7dd7">CMSPCallBase</a>
 

 

