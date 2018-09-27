---
UID: NF:winddi.FONTOBJ_cGetAllGlyphHandles
title: FONTOBJ_cGetAllGlyphHandles function
author: windows-sdk-content
description: The FONTOBJ_cGetAllGlyphHandles function allows the device driver to find every glyph handle of a GDI font.
old-location: display\fontobj_cgetallglyphhandles.htm
tech.root: display
ms.assetid: b3901f9e-14e6-42c2-851c-47c0f386f2d3
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: FONTOBJ_cGetAllGlyphHandles, FONTOBJ_cGetAllGlyphHandles function [Display Devices], display.fontobj_cgetallglyphhandles, gdifncs_b082dddb-7eb3-4676-a05b-8eb731d96fc4.xml, winddi/FONTOBJ_cGetAllGlyphHandles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - FONTOBJ_cGetAllGlyphHandles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FONTOBJ_cGetAllGlyphHandles function


## -description


The <b>FONTOBJ_cGetAllGlyphHandles</b> function allows the device driver to find every glyph handle of a GDI font. 


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/09af2006-51f1-433e-9227-3c99b9860e75">FONTOBJ</a> structure that is to be downloaded.


### -param phg

Pointer to a buffer large enough to hold all the glyph handles in the font. This parameter can be <b>NULL</b>.


## -returns



The return value is the number of glyph handles supported by the font.




## -remarks



A driver uses this function to download an entire font.

The driver must provide a buffer large enough to contain the output. GDI copies all glyph handles belonging to the associated font to this buffer.

The number of glyphs in the font can be determined by calling <a href="https://msdn.microsoft.com/4b952bdc-a496-4ded-9390-9f4b470f3a6c">FONTOBJ_vGetInfo</a>, or by calling <b>FONTOBJ_cGetAllGlyphHandles</b> with the <i>phg</i> parameter set to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/09af2006-51f1-433e-9227-3c99b9860e75">FONTOBJ</a>



<a href="https://msdn.microsoft.com/4b952bdc-a496-4ded-9390-9f4b470f3a6c">FONTOBJ_vGetInfo</a>
 

 

