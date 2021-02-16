---
UID: NF:tom.ITextFont.GetKerning
title: ITextFont::GetKerning (tom.h)
description: Gets the minimum font size at which kerning occurs.
helpviewer_keywords: ["GetKerning","GetKerning method [Windows Controls]","GetKerning method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","GetKerning method","ITextFont.GetKerning","ITextFont::GetKerning","_win32_ITextFont_GetKerning","_win32_ITextFont_GetKerning_cpp","controls.ITextFont_GetKerning","controls._win32_ITextFont_GetKerning","tom/ITextFont::GetKerning"]
old-location: controls\ITextFont_GetKerning.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getkerning.htm
ms.date: 12/05/2018
ms.keywords: GetKerning, GetKerning method [Windows Controls], GetKerning method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetKerning method, ITextFont.GetKerning, ITextFont::GetKerning, _win32_ITextFont_GetKerning, _win32_ITextFont_GetKerning_cpp, controls.ITextFont_GetKerning, controls._win32_ITextFont_GetKerning, tom/ITextFont::GetKerning
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
 - ITextFont::GetKerning
 - tom/ITextFont::GetKerning
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
 - ITextFont.GetKerning
---

# ITextFont::GetKerning


## -description

Gets the minimum font size at which kerning occurs.

## -parameters

### -param pValue

Type: <b>float*</b>

The minimum font size at which kerning occurs, in floating-point points.

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

If the value pointed to by 
				<i>pValue</i> is zero, kerning is off. Positive values turn on pair kerning for font point sizes greater than or equal to the kerning value. For example, the value 1 turns on kerning for all legible sizes, whereas 16 turns on kerning only for font sizes of 16 points and larger.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-setkerning">SetKerning</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>