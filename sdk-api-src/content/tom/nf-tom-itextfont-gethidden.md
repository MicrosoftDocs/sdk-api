---
UID: NF:tom.ITextFont.GetHidden
title: ITextFont::GetHidden (tom.h)
description: Gets whether characters are hidden.
helpviewer_keywords: ["GetHidden","GetHidden method [Windows Controls]","GetHidden method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","GetHidden method","ITextFont.GetHidden","ITextFont::GetHidden","_win32_ITextFont_GetHidden","_win32_ITextFont_GetHidden_cpp","controls.ITextFont_GetHidden","controls._win32_ITextFont_GetHidden","tom/ITextFont::GetHidden"]
old-location: controls\ITextFont_GetHidden.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\gethidden.htm
ms.date: 12/05/2018
ms.keywords: GetHidden, GetHidden method [Windows Controls], GetHidden method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetHidden method, ITextFont.GetHidden, ITextFont::GetHidden, _win32_ITextFont_GetHidden, _win32_ITextFont_GetHidden_cpp, controls.ITextFont_GetHidden, controls._win32_ITextFont_GetHidden, tom/ITextFont::GetHidden
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
 - ITextFont::GetHidden
 - tom/ITextFont::GetHidden
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
 - ITextFont.GetHidden
---

# ITextFont::GetHidden


## -description

Gets whether characters are hidden.

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
<td>Characters are hidden.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Characters are not hidden.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The Hidden property is undefined.</td>
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

This property corresponds to the <b>CFE_HIDDEN</b> effect described in the <a href="/windows/desktop/api/richedit/ns-richedit-charformat2a">CHARFORMAT2</a> structure.

## -see-also

<a href="/windows/desktop/api/richedit/ns-richedit-charformat2a">CHARFORMAT2</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-sethidden">SetHidden</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>