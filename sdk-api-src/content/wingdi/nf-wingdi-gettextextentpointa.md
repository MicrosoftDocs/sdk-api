---
UID: NF:wingdi.GetTextExtentPointA
title: GetTextExtentPointA function (wingdi.h)
description: The GetTextExtentPoint function computes the width and height of the specified string of text. (ANSI)
helpviewer_keywords: ["GetTextExtentPointA", "wingdi/GetTextExtentPointA"]
old-location: gdi\gettextextentpoint.htm
tech.root: gdi
ms.assetid: 731085ce-009d-42e1-885f-2f5151e0f6d3
ms.date: 12/05/2018
ms.keywords: GetTextExtentPoint, GetTextExtentPoint function [Windows GDI], GetTextExtentPointA, GetTextExtentPointW, _win32_GetTextExtentPoint, gdi.gettextextentpoint, wingdi/GetTextExtentPoint, wingdi/GetTextExtentPointA, wingdi/GetTextExtentPointW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTextExtentPointW (Unicode) and GetTextExtentPointA (ANSI)
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
 - GetTextExtentPointA
 - wingdi/GetTextExtentPointA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetTextExtentPoint
 - GetTextExtentPointA
 - GetTextExtentPointW
---

# GetTextExtentPointA function


## -description

The <b>GetTextExtentPoint</b> function computes the width and height of the specified string of text.


<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should call the <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a">GetTextExtentPoint32</a> function, which provides more accurate results.</div>
<div> </div>

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lpString [in]

A pointer to the string that specifies the text. The string does not need to be zero-terminated, since <i>cbString</i> specifies the length of the string.

### -param c [in]

The <a href="/windows/desktop/gdi/specifying-length-of-text-output-string">length of the string</a> pointed to by <i>lpString</i>.

### -param lpsz [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that receives the dimensions of the string, in logical units.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>GetTextExtentPoint</b> function uses the currently selected font to compute the dimensions of the string. The width and height, in logical units, are computed without considering any clipping. Also, this function assumes that the text is horizontal, that is, that the escapement is always 0. This is true for both the horizontal and vertical measurements of the text. Even if using a font specifying a nonzero escapement, this function will not use the angle while computing the text extent. The application must convert it explicitly.

Because some devices kern characters, the sum of the extents of the characters in a string may not be equal to the extent of the string.

The calculated string width takes into account the intercharacter spacing set by the <a href="/windows/desktop/api/wingdi/nf-wingdi-settextcharacterextra">SetTextCharacterExtra</a> function.





> [!NOTE]
> The wingdi.h header defines GetTextExtentPoint as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a">GetTextExtentPoint32</a>



<a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-settextcharacterextra">SetTextCharacterExtra</a>
