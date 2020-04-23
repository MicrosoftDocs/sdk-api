---
UID: NF:tom.ITextFont.GetBackColor
title: ITextFont::GetBackColor (tom.h)
description: Gets the text background (highlight) color.helpviewer_keywords: ["GetBackColor","GetBackColor method [Windows Controls]","GetBackColor method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","GetBackColor method","ITextFont.GetBackColor","ITextFont::GetBackColor","_win32_ITextFont_GetBackColor","_win32_ITextFont_GetBackColor_cpp","controls.ITextFont_GetBackColor","controls._win32_ITextFont_GetBackColor","tom/ITextFont::GetBackColor"]
old-location: controls\ITextFont_GetBackColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getbackcolor.htm
ms.date: 12/05/2018
ms.keywords: GetBackColor, GetBackColor method [Windows Controls], GetBackColor method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetBackColor method, ITextFont.GetBackColor, ITextFont::GetBackColor, _win32_ITextFont_GetBackColor, _win32_ITextFont_GetBackColor_cpp, controls.ITextFont_GetBackColor, controls._win32_ITextFont_GetBackColor, tom/ITextFont::GetBackColor
f1_keywords:
- tom/ITextFont.GetBackColor
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Msftedit.dll
api_name:
- ITextFont.GetBackColor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextFont::GetBackColor


## -description


Gets the text background (highlight) color.


## -parameters




### -param pValue

Type: <b>long*</b>

The text background color. It can be one of the following values. 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>A <a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a> value</td>
<td>The high-order byte is zero, and the three low-order bytes specify an RGB color. </td>
</tr>
<tr>
<td>A value returned by <a href="https://docs.microsoft.com/previous-versions/dd162770(v=vs.85)">PALETTEINDEX</a>
</td>
<td>The high-order byte is 1, and the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a> specifies the index of a logical-color palette entry.</td>
</tr>
<tr>
<td><b>tomAutocolor</b> (-9999997)</td>
<td>Indicates the range uses the default system background color.</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Other Resources</b>



<a href="https://docs.microsoft.com/previous-versions/dd162770(v=vs.85)">PALETTEINDEX</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setbackcolor">SetBackColor</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/text-object-model">Text Object Model</a>
 

 

