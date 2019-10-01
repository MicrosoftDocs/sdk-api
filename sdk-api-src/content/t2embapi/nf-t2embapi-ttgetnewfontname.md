---
UID: NF:t2embapi.TTGetNewFontName
title: TTGetNewFontName function (t2embapi.h)
author: windows-sdk-content
description: Obtains the family name for the font loaded through TTLoadEmbeddedFont.
old-location: gdi\ttgetnewfontname.htm
tech.root: gdi
ms.assetid: 08636992-8dd8-461c-b360-f52a19d845bf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TTGetNewFontName, TTGetNewFontName function [Windows GDI], _win32_TTGetNewFontName, gdi.ttgetnewfontname, t2embapi/TTGetNewFontName
ms.topic: function
f1_keywords: 
 - "t2embapi/TTGetNewFontName"
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
req.lib: T2embed.lib
req.dll: T2embed.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - T2embed.dll
api_name:
 - TTGetNewFontName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TTGetNewFontName function


## -description


Obtains the family name for the font loaded through <a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttloadembeddedfont">TTLoadEmbeddedFont</a>.


## -parameters




### -param phFontReference [in]

Handle that identifies the embedded font that has been installed. The handle references an internal structure, not an Hfont.


### -param wzWinFamilyName [out]

Buffer to hold the new 16-bit-character Microsoft Windows family name.


### -param cchMaxWinName [in]

Length of the string allocated for the Windows name (<i>szWinFamilyName</i>). Must be at least LF_FACESIZE long.


### -param szMacFamilyName [out]

Buffer to hold the new 8-bit-character MacIntosh family name.


### -param cchMaxMacName [in]

Length of the string allocated for the Macintosh name (<i>szMacFamilyName</i>). Must be at least LF_FACESIZE long.


## -returns



If successful, returns E_NONE.

The font family name is a string in <i>szWinFamilyName</i> or <i>szMacFamilyName</i>.

Otherwise, returns an error code described in <a href="https://docs.microsoft.com/windows/desktop/gdi/font-embedding-function-error-messages">Embedding-Function Error Messages</a>.




## -remarks



<div class="alert"><b>Note</b>  This function returns the font family name in the appropriate string buffer, either for Windows or the MacIntosh. The buffer for the other operating system is not used.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttgetembeddedfontinfo">TTGetEmbeddedFontInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttgetembeddingtype">TTGetEmbeddingType</a>



<a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttloadembeddedfont">TTLoadEmbeddedFont</a>
 

 

