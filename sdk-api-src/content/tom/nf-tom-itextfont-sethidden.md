---
UID: NF:tom.ITextFont.SetHidden
title: ITextFont::SetHidden (tom.h)
description: Sets whether characters are hidden.
helpviewer_keywords: ["ITextFont interface [Windows Controls]","SetHidden method","ITextFont.SetHidden","ITextFont::SetHidden","SetHidden","SetHidden method [Windows Controls]","SetHidden method [Windows Controls]","ITextFont interface","_win32_ITextFont_SetHidden","_win32_ITextFont_SetHidden_cpp","controls.ITextFont_SetHidden","controls._win32_ITextFont_SetHidden","tom/ITextFont::SetHidden"]
old-location: controls\ITextFont_SetHidden.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\sethidden.htm
ms.date: 12/05/2018
ms.keywords: ITextFont interface [Windows Controls],SetHidden method, ITextFont.SetHidden, ITextFont::SetHidden, SetHidden, SetHidden method [Windows Controls], SetHidden method [Windows Controls],ITextFont interface, _win32_ITextFont_SetHidden, _win32_ITextFont_SetHidden_cpp, controls.ITextFont_SetHidden, controls._win32_ITextFont_SetHidden, tom/ITextFont::SetHidden
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
 - ITextFont::SetHidden
 - tom/ITextFont::SetHidden
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
 - ITextFont.SetHidden
---

# ITextFont::SetHidden


## -description

Sets whether characters are hidden.

## -parameters

### -param Value [in]

Type: <b>long</b>

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
<td><b>tomToggle</b></td>
<td>Toggle the state of the Hidden property.</td>
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

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-gethidden">GetHidden</a>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>