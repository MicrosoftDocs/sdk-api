---
UID: NF:wingdi.GetTextCharsetInfo
title: GetTextCharsetInfo function (wingdi.h)
description: Retrieves information about the character set of the font that is currently selected into a specified device context.
helpviewer_keywords: ["GetTextCharsetInfo","GetTextCharsetInfo function [Internationalization for Windows Applications]","_win32_GetTextCharsetInfo","intl.gettextcharsetinfo","wingdi/GetTextCharsetInfo"]
old-location: intl\gettextcharsetinfo.htm
tech.root: Intl
ms.assetid: 1c8c114a-b261-457c-b541-4648a8f38ee8
ms.date: 12/05/2018
ms.keywords: GetTextCharsetInfo, GetTextCharsetInfo function [Internationalization for Windows Applications], _win32_GetTextCharsetInfo, intl.gettextcharsetinfo, wingdi/GetTextCharsetInfo
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
 - GetTextCharsetInfo
 - wingdi/GetTextCharsetInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetTextCharsetInfo
---

# GetTextCharsetInfo function


## -description

Retrieves information about the character set of the font that is currently selected into a specified device context.

## -parameters

### -param hdc [in]

Handle to a device context. The function obtains information about the font that is selected into this device context.

### -param lpSig [out, optional]

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-fontsignature">FONTSIGNATURE</a> data structure that receives font-signature information.

If a TrueType font is currently selected into the device context, the <a href="/windows/desktop/api/wingdi/ns-wingdi-fontsignature">FONTSIGNATURE</a> structure receives information that identifies the code page and Unicode subranges for which the font provides glyphs.

If a font other than TrueType is currently selected into the device context, the <a href="/windows/desktop/api/wingdi/ns-wingdi-fontsignature">FONTSIGNATURE</a> structure receives zeros. In this case, the application should use the <a href="/windows/desktop/api/wingdi/nf-wingdi-translatecharsetinfo">TranslateCharsetInfo</a> function to obtain generic font-signature information for the character set.

The <i>lpSig</i> parameter specifies <b>NULL</b> if the application does not require the <a href="/windows/desktop/api/wingdi/ns-wingdi-fontsignature">FONTSIGNATURE</a> information. In this case, the application can also call the       <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextcharset">GetTextCharset</a> function, which is equivalent to calling       <b>GetTextCharsetInfo</b> with <i>lpSig</i> set to <b>NULL</b>.

### -param dwFlags [in]

Reserved; must be set to 0.

## -returns

If successful, returns a value identifying the character set of the font currently selected into the specified device context.

For a list of possible values, see *lfCharSet* field of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfontw">LOGFONT structure</a>.

If the function fails, the return value is **DEFAULT_CHARSET**.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-fontsignature">FONTSIGNATURE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextcharset">GetTextCharset</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-translatecharsetinfo">TranslateCharsetInfo</a>



<a href="/windows/desktop/Intl/unicode-and-character-set-functions">Unicode and Character Set Functions</a>



<a href="/windows/desktop/Intl/unicode-and-character-sets">Unicode and Character Sets</a>
