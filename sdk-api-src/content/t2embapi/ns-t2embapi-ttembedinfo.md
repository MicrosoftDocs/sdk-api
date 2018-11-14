---
UID: NS:t2embapi.TTEMBEDINFO
title: TTEMBEDINFO
author: windows-sdk-content
description: The TTEMBEDINFO structure contains a list of URLs from which the embedded font object may be legitimately referenced.
old-location: gdi\ttembedinfo.htm
tech.root: gdi
ms.assetid: 7e1828bf-c9ed-4120-b91f-b4eb45191e48
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: TTEMBEDINFO, TTEMBEDINFO structure [Windows GDI], _win32_TTEMBEDINFO, gdi.ttembedinfo, t2embapi/TTEMBEDINFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: t2embapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - HeaderDef
api_location:
 - T2embapi.h
api_name:
 - TTEMBEDINFO
product: Windows
targetos: Windows
req.typenames: TTEMBEDINFO
req.redist: 
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
 

 

