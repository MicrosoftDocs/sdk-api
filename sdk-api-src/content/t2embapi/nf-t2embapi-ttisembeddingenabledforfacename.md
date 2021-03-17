---
UID: NF:t2embapi.TTIsEmbeddingEnabledForFacename
title: TTIsEmbeddingEnabledForFacename function (t2embapi.h)
description: Determines whether embedding is enabled for a specified font.
helpviewer_keywords: ["TTIsEmbeddingEnabledForFacename","TTIsEmbeddingEnabledForFacename function [Windows GDI]","_win32_TTIsEmbeddingEnabledForFacename","gdi.ttisembeddingenabledforfacename","t2embapi/TTIsEmbeddingEnabledForFacename"]
old-location: gdi\ttisembeddingenabledforfacename.htm
tech.root: gdi
ms.assetid: 1f494bb1-62c4-45c4-b1a5-df6842d94dcc
ms.date: 12/05/2018
ms.keywords: TTIsEmbeddingEnabledForFacename, TTIsEmbeddingEnabledForFacename function [Windows GDI], _win32_TTIsEmbeddingEnabledForFacename, gdi.ttisembeddingenabledforfacename, t2embapi/TTIsEmbeddingEnabledForFacename
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TTIsEmbeddingEnabledForFacename
 - t2embapi/TTIsEmbeddingEnabledForFacename
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - T2embed.dll
api_name:
 - TTIsEmbeddingEnabledForFacename
---

# TTIsEmbeddingEnabledForFacename function


## -description

Determines whether embedding is enabled for a specified font.

## -parameters

### -param lpszFacename [in]

Pointer to the facename of the font, such as Arial Bold.

### -param pbEnabled [out]

Pointer to a boolean, set upon completion of the function. A nonzero value indicates the font is not in the typeface exclusion list, and, therefore, can be embedded without conflict.

## -returns

If successful, returns E_NONE.

<i>pbEnabled</i> is filled with a boolean that indicates whether embedding is currently enabled within a device context for the specified font.

Otherwise, returns an error code described in <a href="/windows/desktop/gdi/font-embedding-function-error-messages">Embedding-Function Error Messages</a>.

## -remarks

If successful, the client may embed the font.

For additional information on the exclusion list, see the Remarks section of <a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttenableembeddingforfacename">TTEnableEmbeddingForFacename</a>.

## -see-also

<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttenableembeddingforfacename">TTEnableEmbeddingForFacename</a>



<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttgetembeddedfontinfo">TTGetEmbeddedFontInfo</a>



<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttgetembeddingtype">TTGetEmbeddingType</a>



<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttisembeddingenabled">TTIsEmbeddingEnabled</a>