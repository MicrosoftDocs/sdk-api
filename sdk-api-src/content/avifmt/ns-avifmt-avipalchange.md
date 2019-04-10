---
UID: NS:avifmt.__unnamed_struct_3
title: AVIPALCHANGE (avifmt.h)
author: windows-sdk-content
description: The AVIPALCHANGE structure defines a palette change in an AVI file.
old-location: dshow\avipalchange.htm
tech.root: DirectShow
ms.assetid: f8f38fe0-f506-4cf8-9a6d-381cf46b51a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AVIPALCHANGE, AVIPALCHANGE structure [DirectShow], AVIPALCHANGEStructure, _AVIPALchange, avifmt/AVIPALCHANGE, dshow.avipalchange
ms.topic: struct
req.header: avifmt.h
req.include-header: Vfw.h
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
 - HeaderDef
api_location:
 - avifmt.h
api_name:
 - AVIPALCHANGE
product: Windows
targetos: Windows
req.typenames: AVIPALCHANGE
req.redist: 
---

# AVIPALCHANGE structure


## -description


The <b>AVIPALCHANGE</b> structure defines a palette change in an AVI file.
        


## -struct-fields




### -field bFirstEntry

Specifies the index of the first palette entry to change.
          


### -field bNumEntries

Specifies the number of palette entries to change, or zero to change all 256 palette entries.
          


### -field wFlags

Reserved.
          


### -field peNew

Specifies an array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures, of size <b>bNumEntries</b>.
          


## -see-also




<a href="https://msdn.microsoft.com/2d8cf5be-1252-4b58-89b1-f5c53ea17d0e">AVI RIFF File Reference</a>



<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

