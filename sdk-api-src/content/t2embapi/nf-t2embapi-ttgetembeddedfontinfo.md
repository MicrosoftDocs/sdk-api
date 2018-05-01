---
UID: NF:t2embapi.TTGetEmbeddedFontInfo
title: TTGetEmbeddedFontInfo function
author: windows-driver-content
description: Retrieves information about an embedded font, such as embedding permissions. TTGetEmbeddedFontInfo performs the same task as TTLoadEmbeddedFont but does not allocate internal data structures for the embedded font.
old-location: gdi\ttgetembeddedfontinfo.htm
old-project: gdi
ms.assetid: 0ce9ade0-df5b-4a2a-adf6-ca641e27d2bd
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: EMBED_EDITABLE, EMBED_INSTALLABLE, EMBED_NOEMBEDDING, EMBED_PREVIEWPRINT, LICENSE_DEFAULT, LICENSE_EDITABLE, LICENSE_INSTALLABLE, LICENSE_NOEMBEDDING, LICENSE_PREVIEWPRINT, TTEMBED_EMBEDEUDC, TTEMBED_RAW, TTEMBED_SUBSET, TTEMBED_TTCOMPRESSED, TTGetEmbeddedFontInfo, TTGetEmbeddedFontInfo function [Windows GDI], TTLOAD_FONT_SUBSETTED, _win32_TTGetEmbeddedFontInfo, gdi.ttgetembeddedfontinfo, t2embapi/TTGetEmbeddedFontInfo
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
req.typenames: SyncProviderConfiguration
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	T2embed.dll
api_name:
-	TTGetEmbeddedFontInfo
product: Windows
targetos: Windows
req.lib: T2embed.lib
req.dll: T2embed.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TTGetEmbeddedFontInfo function


## -description


Retrieves information about an embedded font, such as embedding permissions. <b>TTGetEmbeddedFontInfo</b> performs the same task as <a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a> but does not allocate internal data structures for the embedded font.


## -parameters




### -param ulFlags [in]

Flags specifying the request. This flag can have zero or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTEMBED_EMBEDEUDC"></a><a id="ttembed_embedeudc"></a><dl>
<dt><b>TTEMBED_EMBEDEUDC</b></dt>
</dl>
</td>
<td width="60%">
Include the associated EUDC font file data with the font structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TTEMBED_RAW"></a><a id="ttembed_raw"></a><dl>
<dt><b>TTEMBED_RAW</b></dt>
</dl>
</td>
<td width="60%">
Return a font structure containing the full character set, non-compressed. This is the default behavior of the function.

</td>
</tr>
<tr>
<td width="40%"><a id="TTEMBED_SUBSET"></a><a id="ttembed_subset"></a><dl>
<dt><b>TTEMBED_SUBSET</b></dt>
</dl>
</td>
<td width="60%">
Return a subsetted font containing only the glyphs indicated by the <i>pusCharCodeSet</i> or <i>pulCharCodeSet</i> parameter. These character codes must be denoted as 16-bit or UCS-4 characters, as appropriate for the parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="TTEMBED_TTCOMPRESSED"></a><a id="ttembed_ttcompressed"></a><dl>
<dt><b>TTEMBED_TTCOMPRESSED</b></dt>
</dl>
</td>
<td width="60%">
Return a compressed font structure.

</td>
</tr>
</table>
 


### -param pulPrivStatus [out]

On completion, indicates embedding privileges of the font. A list of possible values follows:

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
 


### -param ulPrivs [in]

Flag indicating a further restriction of embedding privileges, imposed by the client. See <a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a> for additional information.

This flag must have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LICENSE_PREVIEWPRINT"></a><a id="license_previewprint"></a><dl>
<dt><b>LICENSE_PREVIEWPRINT</b></dt>
</dl>
</td>
<td width="60%">
Preview and Print Embedding.

</td>
</tr>
<tr>
<td width="40%"><a id="LICENSE_EDITABLE"></a><a id="license_editable"></a><dl>
<dt><b>LICENSE_EDITABLE</b></dt>
</dl>
</td>
<td width="60%">
Editable Embedding.

</td>
</tr>
<tr>
<td width="40%"><a id="LICENSE_INSTALLABLE"></a><a id="license_installable"></a><dl>
<dt><b>LICENSE_INSTALLABLE</b></dt>
</dl>
</td>
<td width="60%">
Installable Embedding.

</td>
</tr>
<tr>
<td width="40%"><a id="LICENSE_NOEMBEDDING"></a><a id="license_noembedding"></a><dl>
<dt><b>LICENSE_NOEMBEDDING</b></dt>
</dl>
</td>
<td width="60%">
Restricted License Embedding.

</td>
</tr>
<tr>
<td width="40%"><a id="LICENSE_DEFAULT"></a><a id="license_default"></a><dl>
<dt><b>LICENSE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Use default embedding level.

</td>
</tr>
</table>
 


### -param pulStatus [out]

Pointer to a bitfield containing status information, and is filled upon completion of this function. The status can be zero or the following value:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTLOAD_FONT_SUBSETTED"></a><a id="ttload_font_subsetted"></a><dl>
<dt><b>TTLOAD_FONT_SUBSETTED</b></dt>
</dl>
</td>
<td width="60%">
The font loaded is a subset of the original font.

</td>
</tr>
</table>
 


### -param lpfnReadFromStream

[callback] Pointer to the client-defined callback function that reads the font structure from the document stream.


### -param lpvReadStream [in]

Currently undefined. Reserved for a pointer to the stream (font structure).


### -param pTTLoadInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/7a4beae7-cd30-47e3-b310-d0a79c3c8c36">TTLOADINFO</a> structure containing the URL from which the embedded font object has been obtained.


## -returns



If successful, returns E_NONE.

The location referenced by *<i>pulPrivStatus</i> identifies embedding privileges of the font. The location referenced by *<i>pulStatus</i> identifies whether a subset of the font is embedded.

Otherwise, returns an error code described in <a href="https://msdn.microsoft.com/71effafe-55a9-40ed-81c7-07278eba32d3">Embedding-Function Error Messages</a>.




## -see-also




<a href="https://msdn.microsoft.com/c442447f-221d-4bce-9749-fb9fbe333808">TTGetEmbeddingType</a>



<a href="https://msdn.microsoft.com/08636992-8dd8-461c-b360-f52a19d845bf">TTGetNewFontName</a>



<a href="https://msdn.microsoft.com/7a4beae7-cd30-47e3-b310-d0a79c3c8c36">TTLOADINFO</a>



<a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a>
 

 

