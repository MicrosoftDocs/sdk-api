---
UID: NF:wingdi.SetTextAlign
title: SetTextAlign function (wingdi.h)
description: The SetTextAlign function sets the text-alignment flags for the specified device context.
helpviewer_keywords: ["SetTextAlign","SetTextAlign function [Windows GDI]","TA_BASELINE","TA_BOTTOM","TA_CENTER","TA_LEFT","TA_NOUPDATECP","TA_RIGHT","TA_RTLREADING","TA_TOP","TA_UPDATECP","VTA_BASELINE","VTA_CENTER","_win32_SetTextAlign","gdi.settextalign","wingdi/SetTextAlign"]
old-location: gdi\settextalign.htm
tech.root: gdi
ms.assetid: 422868c5-14c9-4374-9cc5-b7bf91ab9eb4
ms.date: 12/05/2018
ms.keywords: SetTextAlign, SetTextAlign function [Windows GDI], TA_BASELINE, TA_BOTTOM, TA_CENTER, TA_LEFT, TA_NOUPDATECP, TA_RIGHT, TA_RTLREADING, TA_TOP, TA_UPDATECP, VTA_BASELINE, VTA_CENTER, _win32_SetTextAlign, gdi.settextalign, wingdi/SetTextAlign
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
 - SetTextAlign
 - wingdi/SetTextAlign
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetTextAlign
---

# SetTextAlign function


## -description

The <b>SetTextAlign</b> function sets the text-alignment flags for the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param align [in]

The text alignment by using a mask of the values in the following list. Only one flag can be chosen from those that affect horizontal and vertical alignment. In addition, only one of the two flags that alter the current position can be chosen.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TA_BASELINE"></a><a id="ta_baseline"></a><dl>
<dt><b>TA_BASELINE</b></dt>
</dl>
</td>
<td width="60%">
The reference point will be on the base line of the text.

</td>
</tr>
<tr>
<td width="40%"><a id="TA_BOTTOM"></a><a id="ta_bottom"></a><dl>
<dt><b>TA_BOTTOM</b></dt>
</dl>
</td>
<td width="60%">
The reference point will be on the bottom edge of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="TA_TOP"></a><a id="ta_top"></a><dl>
<dt><b>TA_TOP</b></dt>
</dl>
</td>
<td width="60%">
The reference point will be on the top edge of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="TA_CENTER"></a><a id="ta_center"></a><dl>
<dt><b>TA_CENTER</b></dt>
</dl>
</td>
<td width="60%">
The reference point will be aligned horizontally with the center of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="TA_LEFT"></a><a id="ta_left"></a><dl>
<dt><b>TA_LEFT</b></dt>
</dl>
</td>
<td width="60%">
The reference point will be on the left edge of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="TA_RIGHT"></a><a id="ta_right"></a><dl>
<dt><b>TA_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
The reference point will be on the right edge of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="TA_NOUPDATECP"></a><a id="ta_noupdatecp"></a><dl>
<dt><b>TA_NOUPDATECP</b></dt>
</dl>
</td>
<td width="60%">
The current position is not updated after each text output call. The reference point is passed to the text output function.

</td>
</tr>
<tr>
<td width="40%"><a id="TA_RTLREADING"></a><a id="ta_rtlreading"></a><dl>
<dt><b>TA_RTLREADING</b></dt>
</dl>
</td>
<td width="60%">
<b>Middle East language edition of Windows:</b> The text is laid out in right to left reading order, as opposed to the default left to right order. This applies only when the font selected into the device context is either Hebrew or Arabic.

</td>
</tr>
<tr>
<td width="40%"><a id="TA_UPDATECP"></a><a id="ta_updatecp"></a><dl>
<dt><b>TA_UPDATECP</b></dt>
</dl>
</td>
<td width="60%">
The current position is updated after each text output call. The current position is used as the reference point.

</td>
</tr>
</table>
 

When the current font has a vertical default base line, as with Kanji, the following values must be used instead of TA_BASELINE and TA_CENTER.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VTA_BASELINE"></a><a id="vta_baseline"></a><dl>
<dt><b>VTA_BASELINE</b></dt>
</dl>
</td>
<td width="60%">
The reference point will be on the base line of the text.

</td>
</tr>
<tr>
<td width="40%"><a id="VTA_CENTER"></a><a id="vta_center"></a><dl>
<dt><b>VTA_CENTER</b></dt>
</dl>
</td>
<td width="60%">
The reference point will be aligned vertically with the center of the bounding rectangle.

</td>
</tr>
</table>
 

The default values are TA_LEFT, TA_TOP, and TA_NOUPDATECP.

## -returns

If the function succeeds, the return value is the previous text-alignment setting.

If the function fails, the return value is GDI_ERROR.

## -remarks

The <a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> functions use the text-alignment flags to position a string of text on a display or other device. The flags specify the relationship between a reference point and a rectangle that bounds the text. The reference point is either the current position or a point passed to a text output function.

The rectangle that bounds the text is formed by the character cells in the text string.

The best way to get left-aligned text is to use either


```cpp

SetTextAlign (hdc, GetTextAlign(hdc) & (~TA_CENTER))

```


or


```cpp

SetTextAlign (hdc,TA_LEFT | <other flags>)

```


You can also use <b>SetTextAlign</b> (hdc, TA_LEFT) for this purpose, but this loses any vertical or right-to-left settings.

<div class="alert"><b>Note</b>  You should not use <b>SetTextAlign</b> with TA_UPDATECP when you are using <a href="/windows/desktop/api/usp10/nf-usp10-scriptstringout">ScriptStringOut</a>, because selected text is not rendered correctly. If you must use this flag, you can unset and reset it as necessary to avoid the problem.</div>
<div> </div>

#### Examples

For an example, see <a href="/windows/desktop/gdi/setting-the-text-alignment">Setting the Text Alignment</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextalign">GetTextAlign</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptstringout">ScriptStringOut</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a>