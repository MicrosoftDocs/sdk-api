---
UID: NF:t2embapi.TTDeleteEmbeddedFont
title: TTDeleteEmbeddedFont function (t2embapi.h)
description: Releases memory used by an embedded font, hFontReference.
helpviewer_keywords: ["TTDELETE_DONTREMOVEFONT","TTDeleteEmbeddedFont","TTDeleteEmbeddedFont function [Windows GDI]","_win32_TTDeleteEmbeddedFont","gdi.ttdeleteembeddedfont","t2embapi/TTDeleteEmbeddedFont"]
old-location: gdi\ttdeleteembeddedfont.htm
tech.root: gdi
ms.assetid: cbd0945a-3f78-43d2-87f7-18e6e9d00096
ms.date: 12/05/2018
ms.keywords: TTDELETE_DONTREMOVEFONT, TTDeleteEmbeddedFont, TTDeleteEmbeddedFont function [Windows GDI], _win32_TTDeleteEmbeddedFont, gdi.ttdeleteembeddedfont, t2embapi/TTDeleteEmbeddedFont
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
 - TTDeleteEmbeddedFont
 - t2embapi/TTDeleteEmbeddedFont
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
 - TTDeleteEmbeddedFont
---

# TTDeleteEmbeddedFont function


## -description

Releases memory used by an embedded font, <i>hFontReference</i>.

By default, <b>TTDeleteEmbeddedFont</b> also removes the installed version of the font from the user's system. When an installable font is loaded, this function still must be called to release the memory used by the embedded font structure, but a flag can be specified indicating that the font should remain installed on the system.

## -parameters

### -param hFontReference [in]

Handle identifying font, as provided in the <a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttloadembeddedfont">TTLoadEmbeddedFont</a> function.

### -param ulFlags [in]

Flag specifying font deletion options. Currently, this flag can be set to zero or the following value:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTDELETE_DONTREMOVEFONT"></a><a id="ttdelete_dontremovefont"></a><dl>
<dt><b>TTDELETE_DONTREMOVEFONT</b></dt>
</dl>
</td>
<td width="60%">
Do not remove the installed font from the system, but release the memory previously occupied by the embedded font structure.

</td>
</tr>
</table>

### -param pulStatus [out]

Currently undefined.

## -returns

If successful, <b>TTDeleteEmbeddedFont</b> returns a value of E_NONE.

The memory occupied by the embedded font structure is cleared. By default, the font indicated by <i>hFontReference</i> is also permanently removed (uninstalled and deleted) from the system.

Otherwise, returns an error code described in <a href="/windows/desktop/gdi/font-embedding-function-error-messages">Embedding-Function Error Messages</a>.

## -remarks

The client is responsible for calling this function to remove fonts when the embedding privileges do not allow a font to be permanently installed on a user's system.

## -see-also

<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttloadembeddedfont">TTLoadEmbeddedFont</a>