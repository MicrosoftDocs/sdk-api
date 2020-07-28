---
UID: NF:t2embapi.TTEmbedFontFromFileA
title: TTEmbedFontFromFileA function (t2embapi.h)
description: Creates a font structure containing the subsetted wide-character (16-bit) font. An external file provides the font information.
helpviewer_keywords: ["CHARSET_SYMBOL","CHARSET_UNICODE","EMBED_EDITABLE","EMBED_INSTALLABLE","EMBED_NOEMBEDDING","EMBED_PREVIEWPRINT","TTEMBED_EMBEDEUDC","TTEMBED_RAW","TTEMBED_SUBSET","TTEMBED_TTCOMPRESSED","TTEmbedFontFromFileA","TTEmbedFontFromFileA function [Windows GDI]","_win32_TTEmbedFontFromFileA","gdi.ttembedfontfromfilea","t2embapi/TTEmbedFontFromFileA"]
old-location: gdi\ttembedfontfromfilea.htm
tech.root: gdi
ms.assetid: 8bd742e7-e51c-468e-a963-4a90be21a815
ms.date: 12/05/2018
ms.keywords: CHARSET_SYMBOL, CHARSET_UNICODE, EMBED_EDITABLE, EMBED_INSTALLABLE, EMBED_NOEMBEDDING, EMBED_PREVIEWPRINT, TTEMBED_EMBEDEUDC, TTEMBED_RAW, TTEMBED_SUBSET, TTEMBED_TTCOMPRESSED, TTEmbedFontFromFileA, TTEmbedFontFromFileA function [Windows GDI], _win32_TTEmbedFontFromFileA, gdi.ttembedfontfromfilea, t2embapi/TTEmbedFontFromFileA
f1_keywords:
- t2embapi/TTEmbedFontFromFileA
dev_langs:
- c++
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
- TTEmbedFontFromFileA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TTEmbedFontFromFileA function


## -description


Creates a font structure containing the subsetted wide-character (16-bit) font. An external file provides the font information.

This function passes the data to a client-defined callback routine for insertion into the document stream.


## -parameters




### -param hDC [in]

Device context handle.


### -param szFontFileName [in]

The font file name and path to embed. This is an ANSI string.


### -param usTTCIndex [in]

Zero-based index into the font file (TTC) identifying the physical font to embed. If the file contains a single font (such as a TTF or OTF outline file), this parameter should be set to 0.


### -param ulFlags [in]

Flag specifying the embedding request. This flag can have zero or more of the following values.

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
Return a subsetted font containing only the glyphs indicated by the <i>pusCharCodeSet</i> or <i>pulCharCodeSet</i> parameter. These character codes must be denoted as 16-bit or UCS-4 characters as appropriate for the parameter.

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
 


### -param ulCharSet [in]

Flag specifying the character set of the font to be embedded. This flag can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CHARSET_UNICODE"></a><a id="charset_unicode"></a><dl>
<dt><b>CHARSET_UNICODE</b></dt>
</dl>
</td>
<td width="60%">
Unicode character set, requiring 16-bit character encoding.

</td>
</tr>
<tr>
<td width="40%"><a id="CHARSET_SYMBOL"></a><a id="charset_symbol"></a><dl>
<dt><b>CHARSET_SYMBOL</b></dt>
</dl>
</td>
<td width="60%">
Symbol character set, requiring 16-bit character encoding.

</td>
</tr>
</table>
 


### -param pulPrivStatus [out]

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
 


### -param pulStatus [out]

Pointer to a bitfield containing status information about the embedding request. This field is filled upon completion of this function. No bits are currently defined for this parameter.


### -param lpfnWriteToStream

Pointer to the client-defined callback function that writes the font structure to the document stream.  See <a href="https://docs.microsoft.com/previous-versions/dd145225(v=vs.85)">WRITEEMBEDPROC</a>.


### -param lpvWriteStream [in]

A token to represent the output stream.


### -param pusCharCodeSet [in]

Pointer to the buffer containing the optional Unicode character codes for subsetting. This field is only used for subsetting a font and is ignored if theulFlagsfield does not specify TTEMBED_SUBSET.


### -param usCharCodeCount [in]

The number of characters in the list of characters indicated by <i>pusCharCodeSet</i>. This field is only used for subsetting a font and is ignored if the <i>ulFlags</i> field does not specify TTEMBED_SUBSET.


### -param usLanguage [in]

Specifies which language in the name table to keep when subsetting. Set to 0 to keep all languages. This field is only used for subsetting a font and is ignored if the <i>ulFlags</i> field does not specify TTEMBED_SUBSET.


### -param pTTEmbedInfo [in, optional]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/ns-t2embapi-ttembedinfo">TTEMBEDINFO</a> structure containing the URLs from which the embedded font object may be legitimately referenced. If <i>pTTEmbedInfo</i> is <b>NULL</b>, no URLs will be added to the embedded font object and no URL checking will occur when the client calls the <a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttloadembeddedfont">TTLoadEmbeddedFont</a> function.


## -returns



If the embedding is successful, returns E_NONE.

The font structure is incorporated into the document stream by the client. <i>pulPrivStatus</i> is set, indicating the embedding privileges of the font; and <i>pulStatus</i> is set to provide results of the embedding operation.

Otherwise, returns an error code described in <a href="https://docs.microsoft.com/windows/desktop/gdi/font-embedding-function-error-messages">Embedding-Function Error Messages</a>.




## -remarks



This function references a client-defined callback routine for embedding the font structure into the document stream.

Clients are responsible for determining and indicating the character set of the font.

For information on embedding Unicode characters from a device context, see <a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttembedfont">TTEmbedFont</a>; for information on embedding UCS-4 characters from a device context, see <a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttembedfontex">TTEmbedFontEx</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/ns-t2embapi-ttembedinfo">TTEMBEDINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttembedfont">TTEmbedFont</a>



<a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttembedfontex">TTEmbedFontEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttloadembeddedfont">TTLoadEmbeddedFont</a>
 

 

