---
UID: NF:t2embapi.TTGetEmbeddingType
title: TTGetEmbeddingType function (t2embapi.h)
description: Obtains the embedding privileges of a font.
helpviewer_keywords: ["EMBED_EDITABLE","EMBED_INSTALLABLE","EMBED_NOEMBEDDING","EMBED_PREVIEWPRINT","TTGetEmbeddingType","TTGetEmbeddingType function [Windows GDI]","_win32_TTGetEmbeddingType","gdi.ttgetembeddingtype","t2embapi/TTGetEmbeddingType"]
old-location: gdi\ttgetembeddingtype.htm
tech.root: gdi
ms.assetid: c442447f-221d-4bce-9749-fb9fbe333808
ms.date: 12/05/2018
ms.keywords: EMBED_EDITABLE, EMBED_INSTALLABLE, EMBED_NOEMBEDDING, EMBED_PREVIEWPRINT, TTGetEmbeddingType, TTGetEmbeddingType function [Windows GDI], _win32_TTGetEmbeddingType, gdi.ttgetembeddingtype, t2embapi/TTGetEmbeddingType
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
 - TTGetEmbeddingType
 - t2embapi/TTGetEmbeddingType
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
 - TTGetEmbeddingType
---

# TTGetEmbeddingType function


## -description

Obtains the embedding privileges of a font.

## -parameters

### -param hDC [in]

Device context handle.

### -param pulEmbedType [in]

Pointer to flag indicating embedding privileges of the font. This flag can have one of the following values. This function returns the least restrictive license granted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EMBED_PREVIEWPRINT"></a><a id="embed_previewprint"></a><dl>
<dt><b>EMBED_PREVIEWPRINT</b></dt>
</dl>
</td>
<td width="60%">
Preview and Print Embedding.

</td>
</tr>
<tr>
<td width="40%"><a id="EMBED_EDITABLE"></a><a id="embed_editable"></a><dl>
<dt><b>EMBED_EDITABLE</b></dt>
</dl>
</td>
<td width="60%">
Editable Embedding.

</td>
</tr>
<tr>
<td width="40%"><a id="EMBED_INSTALLABLE"></a><a id="embed_installable"></a><dl>
<dt><b>EMBED_INSTALLABLE</b></dt>
</dl>
</td>
<td width="60%">
Installable Embedding.

</td>
</tr>
<tr>
<td width="40%"><a id="EMBED_NOEMBEDDING"></a><a id="embed_noembedding"></a><dl>
<dt><b>EMBED_NOEMBEDDING</b></dt>
</dl>
</td>
<td width="60%">
Restricted License Embedding.

</td>
</tr>
</table>

## -returns

If successful, returns E_NONE.

This function reads the embedding privileges stored in the font and transfers the privileges to <i>pulPrivStatus</i>.

Otherwise, returns an error code described in <a href="/windows/desktop/gdi/font-embedding-function-error-messages">Embedding-Function Error Messages</a>.

## -remarks

Alternatively, an application can determine embedding privileges by using <a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttloadembeddedfont">TTLoadEmbeddedFont</a> and then checking the value returned in <i>pulPrivStatus</i> for success or failure of the function.

## -see-also

<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttgetembeddedfontinfo">TTGetEmbeddedFontInfo</a>



<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttgetnewfontname">TTGetNewFontName</a>



<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttloadembeddedfont">TTLoadEmbeddedFont</a>