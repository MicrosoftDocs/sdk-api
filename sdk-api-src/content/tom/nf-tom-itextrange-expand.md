---
UID: NF:tom.ITextRange.Expand
title: ITextRange::Expand (tom.h)
description: Expands this range so that any partial units it contains are completely contained.
helpviewer_keywords: ["Expand","Expand method [Windows Controls]","Expand method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","Expand method","ITextRange.Expand","ITextRange::Expand","_win32_ITextRange_Expand","_win32_ITextRange_Expand_cpp","controls.ITextRange_Expand","controls._win32_ITextRange_Expand","tom/ITextRange::Expand"]
old-location: controls\ITextRange_Expand.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\expand.htm
ms.date: 12/05/2018
ms.keywords: Expand, Expand method [Windows Controls], Expand method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],Expand method, ITextRange.Expand, ITextRange::Expand, _win32_ITextRange_Expand, _win32_ITextRange_Expand_cpp, controls.ITextRange_Expand, controls._win32_ITextRange_Expand, tom/ITextRange::Expand
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
 - ITextRange::Expand
 - tom/ITextRange::Expand
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
 - ITextRange.Expand
---

# ITextRange::Expand


## -description

Expands this range so that any partial units it contains are completely contained.

## -parameters

### -param Unit

Type: <b>long</b>

Unit to include, if it is partially within the range. The default value is <code>tomWord</code>. For a list of the other <i>Unit</i> values, see the discussion under <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>.

### -param pDelta

Type: <b>long*</b>

The count of characters added to the range. The value can be null.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Unit is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Failure for some other reason.

</td>
</tr>
</table>

## -remarks

For example, if an insertion point is at the beginning, the end, or within a word, <b>ITextRange::Expand</b> expands the range to include that word. If the range already includes one word and part of another, <b>ITextRange::Expand</b> expands the range to include both words. <b>ITextRange::Expand</b> expands the range to include the visible portion of the range's story.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>