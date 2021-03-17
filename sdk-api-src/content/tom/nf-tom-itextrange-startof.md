---
UID: NF:tom.ITextRange.StartOf
title: ITextRange::StartOf (tom.h)
description: Moves the range ends to the start of the first overlapping Unit in the range.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","StartOf method","ITextRange.StartOf","ITextRange::StartOf","StartOf","StartOf method [Windows Controls]","StartOf method [Windows Controls]","ITextRange interface","_win32_ITextRange_StartOf","_win32_ITextRange_StartOf_cpp","controls.ITextRange_StartOf","controls._win32_ITextRange_StartOf","tom/ITextRange::StartOf"]
old-location: controls\ITextRange_StartOf.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\startof.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],StartOf method, ITextRange.StartOf, ITextRange::StartOf, StartOf, StartOf method [Windows Controls], StartOf method [Windows Controls],ITextRange interface, _win32_ITextRange_StartOf, _win32_ITextRange_StartOf_cpp, controls.ITextRange_StartOf, controls._win32_ITextRange_StartOf, tom/ITextRange::StartOf
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
 - ITextRange::StartOf
 - tom/ITextRange::StartOf
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
 - ITextRange.StartOf
---

# ITextRange::StartOf


## -description

Moves the range ends to the start of the first overlapping <i>Unit</i> in the range.

## -parameters

### -param Unit

Type: <b>long</b>

Unit to use in the move operation. For a list of <i>Unit</i> values, see the discussion under <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>.

### -param Extend

Type: <b>long</b>

How to move the ends of the range. It can be one of the following values.
					

<table class="clsStd">
<tr>
<td>0 (or <b>tomMove</b>)</td>
<td>Collapses a nondegenerate range to the start position by moving the insertion point. This is the default.</td>
</tr>
<tr>
<td>1 (or <b>tomExtend</b>)</td>
<td>Moves the start position to the beginning of the overlapping <i>Unit</i>. Does not move the end position. </td>
</tr>
</table>

### -param pDelta

Type: <b>long*</b>

Pointer to a variable that receives the number of characters that the start position is moved. It can be null. On return, <i>pDelta</i> is the signed number of characters that the insertion point or start position is moved. This value is always less than or equal to zero, because the motion is always toward the beginning of the story.

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

If the range is an insertion point on a boundary between <i>Unit</i>s, <b>ITextRange::StartOf</b> does not change the start position. 

The <b>ITextRange::StartOf</b> and <a href="/windows/desktop/api/tom/nf-tom-itextrange-endof">ITextRange::EndOf</a> methods differ from the <a href="/windows/desktop/api/tom/nf-tom-itextselection-homekey">HomeKey</a> and <a href="/windows/desktop/api/tom/nf-tom-itextselection-endkey">EndKey</a> methods in that the latter extend from the active end, whereas <b>ITextRange::StartOf</b> extends from the start position and <b>ITextRange::EndOf</b> extends from the end position.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-endkey">EndKey</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-endof">EndOf</a>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-homekey">HomeKey</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>