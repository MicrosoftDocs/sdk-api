---
UID: NF:t2embapi.TTIsEmbeddingEnabled
title: TTIsEmbeddingEnabled function (t2embapi.h)
author: windows-sdk-content
description: Determines whether the typeface exclusion list contains a specified font.
old-location: gdi\ttisembeddingenabled.htm
tech.root: gdi
ms.assetid: f1e3112b-d840-45eb-bb99-416319ed9e15
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TTIsEmbeddingEnabled, TTIsEmbeddingEnabled function [Windows GDI], _win32_TTIsEmbeddingEnabled, gdi.ttisembeddingenabled, t2embapi/TTIsEmbeddingEnabled
ms.topic: function
f1_keywords: 
 - "t2embapi/TTIsEmbeddingEnabled"
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
 - TTIsEmbeddingEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TTIsEmbeddingEnabled function


## -description


Determines whether the typeface exclusion list contains a specified font.


## -parameters




### -param hDC [in]

Device context handle.


### -param pbEnabled [out]

Pointer to a boolean, set upon completion of the function. A nonzero value indicates the font is not in the typeface exclusion list and, therefore, can be embedded without conflict.


## -returns



If successful, returns E_NONE.

The parameter <i>pbEnabled</i> is filled with a boolean that indicates whether embedding is currently enabled within a device context.

Otherwise, returns an error code described in <a href="https://docs.microsoft.com/windows/desktop/gdi/font-embedding-function-error-messages">Embedding-Function Error Messages</a>.




## -remarks



If the specified font is listed, the client should not embed the font.

For additional information on the exclusion list, see the Remarks section of <a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttenableembeddingforfacename">TTEnableEmbeddingForFacename</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttenableembeddingforfacename">TTEnableEmbeddingForFacename</a>



<a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttgetembeddedfontinfo">TTGetEmbeddedFontInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttgetembeddingtype">TTGetEmbeddingType</a>



<a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttisembeddingenabledforfacename">TTIsEmbeddingEnabledForFacename</a>
 

 

