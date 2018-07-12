---
UID: NF:wingdi.CreateFontIndirectExA
title: CreateFontIndirectExA function
author: windows-sdk-content
description: The CreateFontIndirectEx function specifies a logical font that has the characteristics in the specified structure. The font can subsequently be selected as the current font for any device context.
old-location: gdi\createfontindirectex.htm
old-project: gdi
ms.assetid: 1161b79e-f9c8-4073-97c4-1ccc1a78279b
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: CreateFontIndirectEx, CreateFontIndirectEx function [Windows GDI], CreateFontIndirectExA, CreateFontIndirectExW, _win32_CreateFontIndirectEx, gdi.createfontindirectex, wingdi/CreateFontIndirectEx, wingdi/CreateFontIndirectExA, wingdi/CreateFontIndirectExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateFontIndirectExW (Unicode) and CreateFontIndirectExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateFontIndirectEx
 - CreateFontIndirectExA
 - CreateFontIndirectExW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

