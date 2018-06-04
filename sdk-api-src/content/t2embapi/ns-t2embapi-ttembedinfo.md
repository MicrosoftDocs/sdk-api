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

# TTEMBEDINFO structure


## -description



The <b>TTEMBEDINFO</b> structure contains a list of URLs from which the embedded font object may be legitimately referenced.




## -struct-fields




### -field usStructSize

Size, in bytes, of this structure. The client should set this value to <b>sizeof</b>(TTEMBEDINFO).


### -field usRootStrSize

Size, in wide characters, of <i>pusRootStr</i> including NULL terminator(s).


### -field pusRootStr

One or more full URLs that the embedded font object may be referenced from. Multiple URLs, separated by NULL terminators, can be specified.


## -see-also




<a href="https://msdn.microsoft.com/32f1df87-b742-4b5a-8c61-07e758c7660b">TTEmbedFont</a>



<a href="https://msdn.microsoft.com/2b052d83-0791-4fcb-ab94-7924c751b051">TTEmbedFontEx</a>



<a href="https://msdn.microsoft.com/8bd742e7-e51c-468e-a963-4a90be21a815">TTEmbedFontFromFileA</a>



<a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a>
 

 

