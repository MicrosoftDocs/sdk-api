---
UID: NF:tom.ITextFont.SetForeColor
title: ITextFont::SetForeColor (tom.h)
description: Sets the foreground (text) color.
helpviewer_keywords: ["ITextFont interface [Windows Controls]","SetForeColor method","ITextFont.SetForeColor","ITextFont::SetForeColor","SetForeColor","SetForeColor method [Windows Controls]","SetForeColor method [Windows Controls]","ITextFont interface","_win32_ITextFont_SetForeColor","_win32_ITextFont_SetForeColor_cpp","controls.ITextFont_SetForeColor","controls._win32_ITextFont_SetForeColor","tom/ITextFont::SetForeColor"]
old-location: controls\ITextFont_SetForeColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setforecolor.htm
ms.date: 12/05/2018
ms.keywords: ITextFont interface [Windows Controls],SetForeColor method, ITextFont.SetForeColor, ITextFont::SetForeColor, SetForeColor, SetForeColor method [Windows Controls], SetForeColor method [Windows Controls],ITextFont interface, _win32_ITextFont_SetForeColor, _win32_ITextFont_SetForeColor_cpp, controls.ITextFont_SetForeColor, controls._win32_ITextFont_SetForeColor, tom/ITextFont::SetForeColor
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextFont::SetForeColor
 - tom/ITextFont::SetForeColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont.SetForeColor
---

# ITextFont::SetForeColor


## -description

Sets the foreground (text) color.

## -parameters

### -param Value [in]

Type: <b>long</b>

The new foreground color. It can be one of the following. 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>A <a href="/windows/desktop/gdi/colorref">COLORREF</a> value.</td>
<td>An RGB color.</td>
</tr>
<tr>
<td>A value returned by  <a href="/previous-versions/dd162770(v=vs.85)">PALETTEINDEX</a>
</td>
<td>A palette index.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>No change.</td>
</tr>
<tr>
<td><b>tomAutoColor</b></td>
<td>Use the default foreground color.</td>
</tr>
</table>
 

If 
					<i>Value</i> contains an RGB color, generate the 
					<a href="/windows/desktop/gdi/colorref">COLORREF</a> by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The font object is attached to a range that has been deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-getforecolor">GetForeColor</a>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Other Resources</b>



<a href="/previous-versions/dd162770(v=vs.85)">PALETTEINDEX</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>