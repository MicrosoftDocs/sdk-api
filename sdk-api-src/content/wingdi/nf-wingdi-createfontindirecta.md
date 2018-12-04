---
UID: NF:wingdi.CreateFontIndirectA
title: CreateFontIndirectA function
author: windows-sdk-content
description: The CreateFontIndirect function creates a logical font that has the specified characteristics. The font can subsequently be selected as the current font for any device context.
old-location: gdi\createfontindirect.htm
tech.root: gdi
ms.assetid: b7919fb6-8515-4f1b-af9c-dc7eac381b90
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CreateFontIndirect, CreateFontIndirect function [Windows GDI], CreateFontIndirectA, CreateFontIndirectW, _win32_CreateFontIndirect, gdi.createfontindirect, wingdi/CreateFontIndirect, wingdi/CreateFontIndirectA, wingdi/CreateFontIndirectW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateFontIndirectW (Unicode) and CreateFontIndirectA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Font-l1-1-0.dll
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - CreateFontIndirect
 - CreateFontIndirectA
 - CreateFontIndirectW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateFontIndirectA function


## -description


The <b>CreateFontIndirect</b> function creates a logical font that has the specified characteristics. The font can subsequently be selected as the current font for any device context.


## -parameters




### -param lplf [in]

A pointer to a <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure that defines the characteristics of the logical font.


## -returns



If the function succeeds, the return value is a handle to a logical font.

If the function fails, the return value is <b>NULL</b>.




## -remarks



The <b>CreateFontIndirect</b> function creates a logical font with the characteristics specified in the <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure. When this font is selected by using the <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> function, GDI's font mapper attempts to match the logical font with an existing physical font. If it fails to find an exact match, it provides an alternative whose characteristics match as many of the requested characteristics as possible.

To get the appropriate font on different language versions of the OS, call <a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a> with the desired font characteristics in the <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure, retrieve the appropriate typeface name, and create the font using <a href="https://msdn.microsoft.com/373bac6e-5d4d-4909-8096-2f0e909d2f1d">CreateFont</a> or <b>CreateFontIndirect</b>.

When you no longer need the font, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.

The fonts for many East Asian languages have two typeface names: an English name and a localized name. <a href="https://msdn.microsoft.com/373bac6e-5d4d-4909-8096-2f0e909d2f1d">CreateFont</a> and <b>CreateFontIndirect</b> take the localized typeface name only on a system locale that matches the language, while they take the English typeface name on all other system locales. The best method is to try one name and, on failure, try the other. Note that <a href="https://msdn.microsoft.com/b5dfc38d-c400-4900-a15b-f251815ee346">EnumFonts</a>, <a href="https://msdn.microsoft.com/4960afbb-eeba-4030-ac89-d1ff077bb2f3">EnumFontFamilies</a>, and <a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a> return the English typeface name if the system locale does not match the language of the font.

The font mapper for <a href="https://msdn.microsoft.com/373bac6e-5d4d-4909-8096-2f0e909d2f1d">CreateFont</a>, <b>CreateFontIndirect</b>, and <a href="https://msdn.microsoft.com/1161b79e-f9c8-4073-97c4-1ccc1a78279b">CreateFontIndirectEx</a> recognizes both the English and the localized typeface name, regardless of locale.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/317ea311-0592-432a-87b5-58296de003aa">Creating a Logical Font</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/373bac6e-5d4d-4909-8096-2f0e909d2f1d">CreateFont
      </a>



<a href="https://msdn.microsoft.com/1161b79e-f9c8-4073-97c4-1ccc1a78279b">CreateFontIndirectEx
      </a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject
      </a>



<a href="https://msdn.microsoft.com/4960afbb-eeba-4030-ac89-d1ff077bb2f3">EnumFontFamilies
      </a>



<a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx
      </a>



<a href="https://msdn.microsoft.com/b5dfc38d-c400-4900-a15b-f251815ee346">EnumFonts
      </a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT
      </a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject
      </a>
 

 

