---
UID: NF:winuser.DrawStateW
title: DrawStateW function (winuser.h)
description: The DrawState function displays an image and applies a visual effect to indicate a state, such as a disabled or default state. (Unicode)
helpviewer_keywords: ["DSS_DISABLED", "DSS_HIDEPREFIX", "DSS_MONO", "DSS_NORMAL", "DSS_PREFIXONLY", "DSS_RIGHT", "DSS_UNION", "DST_BITMAP", "DST_COMPLEX", "DST_ICON", "DST_PREFIXTEXT", "DST_TEXT", "DrawState", "DrawState function [Windows GDI]", "DrawStateW", "_win32_DrawState", "gdi.drawstate", "winuser/DrawState", "winuser/DrawStateW"]
old-location: gdi\drawstate.htm
tech.root: gdi
ms.assetid: b92150be-8264-4ea8-a2ea-d70b7fba6361
ms.date: 12/05/2018
ms.keywords: DSS_DISABLED, DSS_HIDEPREFIX, DSS_MONO, DSS_NORMAL, DSS_PREFIXONLY, DSS_RIGHT, DSS_UNION, DST_BITMAP, DST_COMPLEX, DST_ICON, DST_PREFIXTEXT, DST_TEXT, DrawState, DrawState function [Windows GDI], DrawStateA, DrawStateW, _win32_DrawState, gdi.drawstate, winuser/DrawState, winuser/DrawStateA, winuser/DrawStateW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DrawStateW (Unicode) and DrawStateA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawStateW
 - winuser/DrawStateW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - ext-ms-win-ntuser-misc-l1-5-1.dll
 - ext-ms-win-ntuser-misc-l1-5-0.dll
 - ext-ms-win-ntuser-misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-2-0.dll
 - ext-ms-win-ntuser-misc-l1-1-0.dll
 - user32.dll
api_name:
 - DrawState
 - DrawStateA
 - DrawStateW
---

# DrawStateW function


## -description

The <b>DrawState</b> function displays an image and applies a visual effect to indicate a state, such as a disabled or default state.

## -parameters

### -param hdc [in]

A handle to the device context to draw in.

### -param hbrFore [in]

A handle to the brush used to draw the image, if the state specified by the <i>fuFlags</i> parameter is DSS_MONO. This parameter is ignored for other states.

### -param qfnCallBack [in]

A pointer to an application-defined callback function used to render the image. This parameter is required if the image type in <i>fuFlags</i> is DST_COMPLEX. It is optional and can be <b>NULL</b> if the image type is DST_TEXT. For all other image types, this parameter is ignored. For more information about the callback function, see the <a href="/windows/desktop/api/winuser/nc-winuser-drawstateproc">DrawStateProc</a> function.

### -param lData [in]

Information about the image. The meaning of this parameter depends on the image type.

### -param wData [in]

Information about the image. The meaning of this parameter depends on the image type. It is, however, zero extended for use with the <a href="/windows/desktop/api/winuser/nc-winuser-drawstateproc">DrawStateProc</a> function.

### -param x [in]

The horizontal location, in device units, at which to draw the image.

### -param y [in]

The vertical location, in device units, at which to draw the image.

### -param cx [in]

The width of the image, in device units. This parameter is required if the image type is DST_COMPLEX. Otherwise, it can be zero to calculate the width of the image.

### -param cy [in]

The height of the image, in device units. This parameter is required if the image type is DST_COMPLEX. Otherwise, it can be zero to calculate the height of the image.

### -param uFlags [in]

The image type and state. This parameter can be one of the following type values.

<table>
<tr>
<th>Value (type)</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DST_BITMAP"></a><a id="dst_bitmap"></a><dl>
<dt><b>DST_BITMAP</b></dt>
</dl>
</td>
<td width="60%">
The image is a bitmap. The <i>lData</i> parameter is the bitmap handle. Note that the bitmap cannot already be selected into an existing device context.

</td>
</tr>
<tr>
<td width="40%"><a id="DST_COMPLEX"></a><a id="dst_complex"></a><dl>
<dt><b>DST_COMPLEX</b></dt>
</dl>
</td>
<td width="60%">
The image is application defined. To render the image, <b>DrawState</b> calls the callback function specified by the <i>lpOutputFunc</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="DST_ICON"></a><a id="dst_icon"></a><dl>
<dt><b>DST_ICON</b></dt>
</dl>
</td>
<td width="60%">
The image is an icon. The <i>lData</i> parameter is the icon handle.

</td>
</tr>
<tr>
<td width="40%"><a id="DST_PREFIXTEXT"></a><a id="dst_prefixtext"></a><dl>
<dt><b>DST_PREFIXTEXT</b></dt>
</dl>
</td>
<td width="60%">
The image is text that may contain an accelerator mnemonic. <b>DrawState</b> interprets the ampersand (&amp;) prefix character as a directive to underscore the character that follows. The <i>lData</i> parameter is a pointer to the string, and the <i>wData</i> parameter specifies the length. If <i>wData</i> is zero, the string must be null-terminated.

</td>
</tr>
<tr>
<td width="40%"><a id="DST_TEXT"></a><a id="dst_text"></a><dl>
<dt><b>DST_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The image is text. The <i>lData</i> parameter is a pointer to the string, and the <i>wData</i> parameter specifies the length. If <i>wData</i> is zero, the string must be null-terminated.

</td>
</tr>
</table>
 

This parameter can also be one of the following state values.

<table>
<tr>
<th>Value (state)</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DSS_DISABLED"></a><a id="dss_disabled"></a><dl>
<dt><b>DSS_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Embosses the image.

</td>
</tr>
<tr>
<td width="40%"><a id="DSS_HIDEPREFIX"></a><a id="dss_hideprefix"></a><dl>
<dt><b>DSS_HIDEPREFIX</b></dt>
</dl>
</td>
<td width="60%">
Ignores the ampersand (&amp;) prefix character in the text, thus the letter that follows will not be underlined. This must be used with DST_PREFIXTEXT.

</td>
</tr>
<tr>
<td width="40%"><a id="DSS_MONO"></a><a id="dss_mono"></a><dl>
<dt><b>DSS_MONO</b></dt>
</dl>
</td>
<td width="60%">
Draws the image using the brush specified by the <i>hbr</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="DSS_NORMAL"></a><a id="dss_normal"></a><dl>
<dt><b>DSS_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
Draws the image without any modification.

</td>
</tr>
<tr>
<td width="40%"><a id="DSS_PREFIXONLY"></a><a id="dss_prefixonly"></a><dl>
<dt><b>DSS_PREFIXONLY</b></dt>
</dl>
</td>
<td width="60%">
Draws only the underline at the position of the letter after the ampersand (&amp;) prefix character. No text in the string is drawn. This must be used with DST_PREFIXTEXT.

</td>
</tr>
<tr>
<td width="40%"><a id="DSS_RIGHT"></a><a id="dss_right"></a><dl>
<dt><b>DSS_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Aligns the text to the right.

</td>
</tr>
<tr>
<td width="40%"><a id="DSS_UNION"></a><a id="dss_union"></a><dl>
<dt><b>DSS_UNION</b></dt>
</dl>
</td>
<td width="60%">
Dithers the image.

</td>
</tr>
</table>
 

For all states except DSS_NORMAL, the image is converted to monochrome before the visual effect is applied.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/api/winuser/nc-winuser-drawstateproc">DrawStateProc</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>

## -remarks

> [!NOTE]
> The winuser.h header defines DrawState as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
