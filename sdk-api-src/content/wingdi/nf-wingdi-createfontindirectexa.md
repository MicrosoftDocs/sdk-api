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

# CreateFontIndirectExA function


## -description


The <b>CreateFontIndirectEx</b> function specifies a logical font that has the characteristics in the specified structure. The font can subsequently be selected as the current font for any device context.


## -parameters




### -param ENUMLOGFONTEXDVA

TBD




#### - penumlfex [in]

Pointer to an <a href="https://msdn.microsoft.com/8d483f52-250e-4c4f-83cf-ff952bb84fd3">ENUMLOGFONTEXDV</a> structure that defines the characteristics of a multiple master font.

Note, this function ignores the <b>elfDesignVector</b> member in <a href="https://msdn.microsoft.com/8d483f52-250e-4c4f-83cf-ff952bb84fd3">ENUMLOGFONTEXDV</a>.


## -returns



If the function succeeds, the return value is the handle to the new <a href="https://msdn.microsoft.com/8d483f52-250e-4c4f-83cf-ff952bb84fd3">ENUMLOGFONTEXDV</a> structure.

If the function fails, the return value is zero. No extended error information is available.




## -remarks



The <b>CreateFontIndirectEx</b> function creates a logical font with the characteristics specified in the <a href="https://msdn.microsoft.com/8d483f52-250e-4c4f-83cf-ff952bb84fd3">ENUMLOGFONTEXDV</a> structure. When this font is selected by using the <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> function, GDI's font mapper attempts to match the logical font with an existing physical font. If it fails to find an exact match, it provides an alternative whose characteristics match as many of the requested characteristics as possible.

When you no longer need the font, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.

The font mapper for <a href="https://msdn.microsoft.com/373bac6e-5d4d-4909-8096-2f0e909d2f1d">CreateFont</a>, <a href="https://msdn.microsoft.com/b7919fb6-8515-4f1b-af9c-dc7eac381b90">CreateFontIndirect</a>, and <b>CreateFontIndirectEx</b> recognizes both the English and the localized typeface name, regardless of locale.




## -see-also




<a href="https://msdn.microsoft.com/373bac6e-5d4d-4909-8096-2f0e909d2f1d">
        CreateFont
      </a>



<a href="https://msdn.microsoft.com/b7919fb6-8515-4f1b-af9c-dc7eac381b90">
        CreateFontIndirect
      </a>



<a href="https://msdn.microsoft.com/8d483f52-250e-4c4f-83cf-ff952bb84fd3">
        ENUMLOGFONTEXDV
      </a>



<a href="https://msdn.microsoft.com/4960afbb-eeba-4030-ac89-d1ff077bb2f3">
        EnumFontFamilies
      </a>



<a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">
        EnumFontFamiliesEx
      </a>



<a href="https://msdn.microsoft.com/b5dfc38d-c400-4900-a15b-f251815ee346">
        EnumFonts
      </a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>
 

 

