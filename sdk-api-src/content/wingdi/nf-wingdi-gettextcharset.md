---
UID: NF:wingdi.GetTextCharset
title: GetTextCharset function (wingdi.h)
description: Retrieves a character set identifier for the font that is currently selected into a specified device context.
helpviewer_keywords: ["GetTextCharset","GetTextCharset function [Internationalization for Windows Applications]","_win32_GetTextCharset","intl.gettextcharset","wingdi/GetTextCharset"]
old-location: intl\gettextcharset.htm
tech.root: Intl
ms.assetid: 11040353-a2ea-42fe-aa89-3438ffc1fea6
ms.date: 12/05/2018
ms.keywords: GetTextCharset, GetTextCharset function [Internationalization for Windows Applications], _win32_GetTextCharset, intl.gettextcharset, wingdi/GetTextCharset
req.header: wingdi.h
req.include-header: Windows.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetTextCharset
 - wingdi/GetTextCharset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - Ext-MS-Win-GDI-Font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetTextCharset
---

# GetTextCharset function


## -description

Retrieves a character set identifier for the font that is currently selected into a specified device context.
<div class="alert"><b>Note</b>  A call to this function is equivalent to a call to <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextcharsetinfo">GetTextCharsetInfo</a> passing <b>NULL</b> for the data buffer.</div><div> </div>

## -parameters

### -param hdc [in]

Handle to a device context. The function obtains a character set identifier for the font that is selected into this device context.

## -returns

If successful, returns a value identifying the character set of the font that is currently selected into the specified device context.

For a list of possible values, see *lfCharSet* field of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfontw">LOGFONT structure</a>.

If the function fails, it returns **DEFAULT_CHARSET**.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextcharsetinfo">GetTextCharsetInfo</a>



<a href="/windows/desktop/Intl/unicode-and-character-set-functions">Unicode and Character Set Functions</a>



<a href="/windows/desktop/Intl/unicode-and-character-sets">Unicode and Character Sets</a>
