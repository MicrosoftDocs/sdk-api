---
UID: NF:tom.ITextFont.GetShadow
title: ITextFont::GetShadow (tom.h)
description: Gets whether characters are displayed as shadowed characters.
helpviewer_keywords: ["GetShadow","GetShadow method [Windows Controls]","GetShadow method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","GetShadow method","ITextFont.GetShadow","ITextFont::GetShadow","_win32_ITextFont_GetShadow","_win32_ITextFont_GetShadow_cpp","controls.ITextFont_GetShadow","controls._win32_ITextFont_GetShadow","tom/ITextFont::GetShadow"]
old-location: controls\ITextFont_GetShadow.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getshadow.htm
ms.date: 12/05/2018
ms.keywords: GetShadow, GetShadow method [Windows Controls], GetShadow method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetShadow method, ITextFont.GetShadow, ITextFont::GetShadow, _win32_ITextFont_GetShadow, _win32_ITextFont_GetShadow_cpp, controls.ITextFont_GetShadow, controls._win32_ITextFont_GetShadow, tom/ITextFont::GetShadow
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
 - ITextFont::GetShadow
 - tom/ITextFont::GetShadow
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
 - ITextFont.GetShadow
---

# ITextFont::GetShadow


## -description

Gets whether characters are displayed as shadowed characters.

## -parameters

### -param pValue

Type: <b>long*</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that can be one of the following.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Characters are displayed as shadowed characters.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Characters are not displayed as shadowed characters.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The Shadow property is undefined.</td>
</tr>
</table>

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

This property corresponds to the <b>CFE_SHADOW</b> effect described in the <a href="/windows/desktop/api/richedit/ns-richedit-charformat2a">CHARFORMAT2</a> structure.

## -see-also

<a href="/windows/desktop/api/richedit/ns-richedit-charformat2a">CHARFORMAT2</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-setshadow">SetShadow</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>