---
UID: NF:tom.ITextFont.GetPosition
title: ITextFont::GetPosition (tom.h)
description: Gets the amount that characters are offset vertically relative to the baseline.
helpviewer_keywords: ["GetPosition","GetPosition method [Windows Controls]","GetPosition method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","GetPosition method","ITextFont.GetPosition","ITextFont::GetPosition","_win32_ITextFont_GetPosition","_win32_ITextFont_GetPosition_cpp","controls.ITextFont_GetPosition","controls._win32_ITextFont_GetPosition","tom/ITextFont::GetPosition"]
old-location: controls\ITextFont_GetPosition.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getposition.htm
ms.date: 12/05/2018
ms.keywords: GetPosition, GetPosition method [Windows Controls], GetPosition method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetPosition method, ITextFont.GetPosition, ITextFont::GetPosition, _win32_ITextFont_GetPosition, _win32_ITextFont_GetPosition_cpp, controls.ITextFont_GetPosition, controls._win32_ITextFont_GetPosition, tom/ITextFont::GetPosition
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
 - ITextFont::GetPosition
 - tom/ITextFont::GetPosition
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
 - ITextFont.GetPosition
---

# ITextFont::GetPosition


## -description

Gets the amount that characters are  offset vertically relative to the baseline.

## -parameters

### -param pValue

Type: <b>float*</b>

The amount of vertical offset, in floating-point points.

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
</table>

## -remarks

Displayed text typically has a zero value for this property. Positive values raise the text, and negative values lower it.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-setposition">SetPosition</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>