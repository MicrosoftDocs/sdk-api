---
UID: NF:t2embapi.TTGetEmbeddingType
title: TTGetEmbeddingType function
author: windows-sdk-content
description: Obtains the embedding privileges of a font.
old-location: gdi\ttgetembeddingtype.htm
tech.root: gdi
ms.assetid: c442447f-221d-4bce-9749-fb9fbe333808
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EMBED_EDITABLE, EMBED_INSTALLABLE, EMBED_NOEMBEDDING, EMBED_PREVIEWPRINT, TTGetEmbeddingType, TTGetEmbeddingType function [Windows GDI], _win32_TTGetEmbeddingType, gdi.ttgetembeddingtype, t2embapi/TTGetEmbeddingType
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - TTGetEmbeddingType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Otherwise, returns an error code described in <a href="https://msdn.microsoft.com/71effafe-55a9-40ed-81c7-07278eba32d3">Embedding-Function Error Messages</a>.




## -remarks



Alternatively, an application can determine embedding privileges by using <a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a> and then checking the value returned in <i>pulPrivStatus</i> for success or failure of the function.




## -see-also




<a href="https://msdn.microsoft.com/0ce9ade0-df5b-4a2a-adf6-ca641e27d2bd">TTGetEmbeddedFontInfo</a>



<a href="https://msdn.microsoft.com/08636992-8dd8-461c-b360-f52a19d845bf">TTGetNewFontName</a>



<a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a>
 

 

