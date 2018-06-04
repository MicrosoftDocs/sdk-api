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

# FONTOBJ_cGetAllGlyphHandles function


## -description


The <b>FONTOBJ_cGetAllGlyphHandles</b> function allows the device driver to find every glyph handle of a GDI font. 


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure that is to be downloaded.


### -param phg

Pointer to a buffer large enough to hold all the glyph handles in the font. This parameter can be <b>NULL</b>.


## -returns



The return value is the number of glyph handles supported by the font.




## -remarks



A driver uses this function to download an entire font.

The driver must provide a buffer large enough to contain the output. GDI copies all glyph handles belonging to the associated font to this buffer.

The number of glyphs in the font can be determined by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff566013">FONTOBJ_vGetInfo</a>, or by calling <b>FONTOBJ_cGetAllGlyphHandles</b> with the <i>phg</i> parameter set to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566013">FONTOBJ_vGetInfo</a>
 

 

