---
UID: NF:t2embapi.TTLoadEmbeddedFont
title: TTLoadEmbeddedFont function (t2embapi.h)
description: Reads an embedded font from the document stream and installs it. Also allows a client to further restrict embedding privileges of the font.
helpviewer_keywords: ["EMBED_EDITABLE","EMBED_INSTALLABLE","EMBED_NOEMBEDDING","EMBED_PREVIEWPRINT","LICENSE_DEFAULT","LICENSE_EDITABLE","LICENSE_INSTALLABLE","LICENSE_NOEMBEDDING","LICENSE_PREVIEWPRINT","TTLOAD_FONT_IN_SYSSTARTUP","TTLOAD_FONT_SUBSETTED","TTLOAD_PRIVATE","TTLoadEmbeddedFont","TTLoadEmbeddedFont function [Windows GDI]","_win32_TTLoadEmbeddedFont","gdi.ttloadembeddedfont","t2embapi/TTLoadEmbeddedFont"]
old-location: gdi\ttloadembeddedfont.htm
tech.root: gdi
ms.assetid: 85181d86-bc18-4948-bc7d-65c2d71efefb
ms.date: 12/05/2018
ms.keywords: EMBED_EDITABLE, EMBED_INSTALLABLE, EMBED_NOEMBEDDING, EMBED_PREVIEWPRINT, LICENSE_DEFAULT, LICENSE_EDITABLE, LICENSE_INSTALLABLE, LICENSE_NOEMBEDDING, LICENSE_PREVIEWPRINT, TTLOAD_FONT_IN_SYSSTARTUP, TTLOAD_FONT_SUBSETTED, TTLOAD_PRIVATE, TTLoadEmbeddedFont, TTLoadEmbeddedFont function [Windows GDI], _win32_TTLoadEmbeddedFont, gdi.ttloadembeddedfont, t2embapi/TTLoadEmbeddedFont
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
 - TTLoadEmbeddedFont
 - t2embapi/TTLoadEmbeddedFont
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
 - TTLoadEmbeddedFont
---

# TTLoadEmbeddedFont function


## -description

Reads an embedded font from the document stream and installs it. Also allows a client to further restrict embedding privileges of the font.

## -parameters

### -param phFontReference [out]

A pointer to a handle that identifies the installed embedded font. This handle references an internal structure, not an Hfont.

### -param ulFlags [in]

A flag specifying loading and installation options. Currently, this flag can be set to zero or the following value:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTLOAD_PRIVATE"></a><a id="ttload_private"></a><dl>
<dt><b>TTLOAD_PRIVATE</b></dt>
</dl>
</td>
<td width="60%">
Load the font so that it is not enumerated to the user. If the font is not installable, it will remain private.

</td>
</tr>
</table>

### -param pulPrivStatus [out]

A pointer to flag indicating embedding privileges of the font. This flag is written upon completion of this function and can have one of the following values. This function returns the least restrictive license granted.

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
Preview and Print Embedding. The font may be embedded within documents, but must only be installed temporarily on the remote system. A document containing this type of font can only be opened as read-only. The application must not allow the user to edit the document. The document can only be viewed and/or printed.

</td>
</tr>
<tr>
<td width="40%"><a id="EMBED_EDITABLE"></a><a id="embed_editable"></a><dl>
<dt><b>EMBED_EDITABLE</b></dt>
</dl>
</td>
<td width="60%">
Editable Embedding. The font may be embedded within documents, but must only be installed temporarily on the remote system. A document containing this type of font may be opened "read/write," with editing permitted.

</td>
</tr>
<tr>
<td width="40%"><a id="EMBED_INSTALLABLE"></a><a id="embed_installable"></a><dl>
<dt><b>EMBED_INSTALLABLE</b></dt>
</dl>
</td>
<td width="60%">
Installable Embedding. The font may be embedded and permanently installed on the remote system. The user of the remote system acquires the identical rights, obligations, and licenses for that font as the original purchaser of the font, and is subject to the same end-user license agreement, copyright, design patent, and/or trademark as was the original purchaser.

</td>
</tr>
<tr>
<td width="40%"><a id="EMBED_NOEMBEDDING"></a><a id="embed_noembedding"></a><dl>
<dt><b>EMBED_NOEMBEDDING</b></dt>
</dl>
</td>
<td width="60%">
Restricted License Embedding. The font must not be modified, embedded, or exchanged in any manner without first obtaining permission of the legal owner.

</td>
</tr>
</table>

### -param ulPrivs [in]

A flag indicating a further restriction of embedding privileges, imposed by the client loading the font. This flag must have one of the following values.

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

A pointer to a bitfield containing status information about the <b>TTLoadEmbeddedFont</b> request. This field is filled upon completion of this function and can have zero or more of the following values.

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
<tr>
<td width="40%"><a id="TTLOAD_FONT_IN_SYSSTARTUP"></a><a id="ttload_font_in_sysstartup"></a><dl>
<dt><b>TTLOAD_FONT_IN_SYSSTARTUP</b></dt>
</dl>
</td>
<td width="60%">
The font loaded was labeled as installable and has been added to the registry so it will be available upon startup.

</td>
</tr>
</table>

### -param lpfnReadFromStream [in]

A pointer to the client-defined callback function that reads the font structure from the document stream.

### -param lpvReadStream [in]

A pointer to the stream (font structure).

### -param szWinFamilyName [in, optional]

A pointer to the new 16-bit-character Unicode Microsoft Windows family name of the font. Set to <b>NULL</b> to use existing name. When changing the name of a font upon loading, you must supply both this parameter and the <i>szMacFamilyName</i> parameter.

### -param szMacFamilyName [in, optional]

A pointer to the new 8-bit-character Macintosh family name of the font. Set to <b>NULL</b> to use existing name. When changing the name of a font upon loading, you must supply both this parameter and the <i>szWinFamilyName</i> parameter.

### -param pTTLoadInfo [in, optional]

A pointer to a <a href="/windows/desktop/api/t2embapi/ns-t2embapi-ttloadinfo">TTLOADINFO</a> structure containing the URL from which the embedded font object has been obtained. If this value does not match one of those contained in the <a href="/windows/desktop/api/t2embapi/ns-t2embapi-ttembedinfo">TTEMBEDINFO</a> structure, the font will not load successfully.

## -returns

If successful, returns E_NONE.

If font loading is successful, a font indicated by <i>phFontReference</i> is created from the font structure with the names referenced in <i>szWinFamilyName</i> and <i>szMacFamilyName</i>. <i>pulPrivStatus</i> is set indicating the embedding privileges of the font; and <i>pulStatus</i> may be set indicating status information about the font loading operation.

Otherwise, returns an error code described in <a href="/windows/desktop/gdi/font-embedding-function-error-messages">Embedding Function Error Messages</a>.

## -remarks

To assist a client in determining whether an embedded font is already installed on the system, the font loading function will return an error message indicating a font with the same name exists on the system (E_FONTNAMEALREADYEXISTS), and if that font has the same checksum as the embedded font (E_FONTALREADYEXISTS). The client then has two options:

<ol>
<li>Assume that the installed font is really the same as the embedded font and covers the same subsets.</li>
<li>Force the embedded font to be installed with a different name to avoid incompatibilities with the font already on the system.</li>
</ol>
To change the name of an embedded font prior to installing, the client must supply both the 8-bit-character and 16-bit-character name strings as parameters. The font name will be changed in the name table of the newly installed font. The new name is only available to the client and will not be enumerated to the user.

To use the existing name of the embedded font, the name string parameters need to be set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttdeleteembeddedfont">TTDeleteEmbeddedFont</a>



<a href="/windows/desktop/api/t2embapi/ns-t2embapi-ttembedinfo">TTEMBEDINFO</a>



<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttgetembeddingtype">TTGetEmbeddingType</a>



<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttgetnewfontname">TTGetNewFontName</a>



<a href="/windows/desktop/api/t2embapi/ns-t2embapi-ttloadinfo">TTLOADINFO</a>