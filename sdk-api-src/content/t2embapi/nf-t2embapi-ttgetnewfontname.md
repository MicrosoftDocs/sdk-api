---
UID: NF:t2embapi.TTGetNewFontName
title: TTGetNewFontName function
author: windows-sdk-content
description: Obtains the family name for the font loaded through TTLoadEmbeddedFont.
old-location: gdi\ttgetnewfontname.htm
old-project: gdi
ms.assetid: 08636992-8dd8-461c-b360-f52a19d845bf
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: TTGetNewFontName, TTGetNewFontName function [Windows GDI], _win32_TTGetNewFontName, gdi.ttgetnewfontname, t2embapi/TTGetNewFontName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: SyncProviderConfiguration
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	T2embed.dll
api_name:
-	TTGetNewFontName
product: Windows
targetos: Windows
req.lib: T2embed.lib
req.dll: T2embed.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TTGetNewFontName function


## -description


Obtains the family name for the font loaded through <a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a>.


## -parameters




### -param phFontReference [in]

Handle that identifies the embedded font that has been installed. The handle references an internal structure, not an Hfont.


### -param wzWinFamilyName

TBD


### -param cchMaxWinName [in]

Length of the string allocated for the Windows name (<i>szWinFamilyName</i>). Must be at least LF_FACESIZE long.


### -param szMacFamilyName [out]

Buffer to hold the new 8-bit-character MacIntosh family name.


### -param cchMaxMacName [in]

Length of the string allocated for the Macintosh name (<i>szMacFamilyName</i>). Must be at least LF_FACESIZE long.


#### - szWinFamilyName [out]

Buffer to hold the new 16-bit-character Microsoft Windows family name.


## -returns



If successful, returns E_NONE.

The font family name is a string in <i>szWinFamilyName</i> or <i>szMacFamilyName</i>.

Otherwise, returns an error code described in <a href="https://msdn.microsoft.com/71effafe-55a9-40ed-81c7-07278eba32d3">Embedding-Function Error Messages</a>.




## -remarks



<div class="alert"><b>Note</b>  This function returns the font family name in the appropriate string buffer, either for Windows or the MacIntosh. The buffer for the other operating system is not used.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0ce9ade0-df5b-4a2a-adf6-ca641e27d2bd">TTGetEmbeddedFontInfo</a>



<a href="https://msdn.microsoft.com/c442447f-221d-4bce-9749-fb9fbe333808">TTGetEmbeddingType</a>



<a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a>
 

 

