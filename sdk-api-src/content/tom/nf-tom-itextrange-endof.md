---
UID: NF:tom.ITextRange.EndOf
title: ITextRange::EndOf (tom.h)
description: Moves this range's ends to the end of the last overlapping Unit in the range.
helpviewer_keywords: ["EndOf","EndOf method [Windows Controls]","EndOf method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","EndOf method","ITextRange.EndOf","ITextRange::EndOf","_win32_ITextRange_EndOf","_win32_ITextRange_EndOf_cpp","controls.ITextRange_EndOf","controls._win32_ITextRange_EndOf","tom/ITextRange::EndOf"]
old-location: controls\ITextRange_EndOf.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\endof.htm
ms.date: 12/05/2018
ms.keywords: EndOf, EndOf method [Windows Controls], EndOf method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],EndOf method, ITextRange.EndOf, ITextRange::EndOf, _win32_ITextRange_EndOf, _win32_ITextRange_EndOf_cpp, controls.ITextRange_EndOf, controls._win32_ITextRange_EndOf, tom/ITextRange::EndOf
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
 - ITextRange::EndOf
 - tom/ITextRange::EndOf
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
 - ITextRange.EndOf
---

# ITextRange::EndOf


## -description

Moves this range's ends to the end of the last overlapping <i>Unit</i> in the range.

## -parameters

### -param Unit

Type: <b>long</b>

Unit to use. Default value: <i>tomWord</i>. For a list of the other <i>Unit</i> values, see the discussion under <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>.

### -param Extend

Type: <b>long</b>

Indicator of how the shifting of the range ends is to proceed. It can be one of the following. 
					

<table class="clsStd">
<tr>
<td>0 or <i>tomMove</i></td>
<td>Collapses a nondegenerate range to the End of the original range by moving the insertion point. This is the default.</td>
</tr>
<tr>
<td>1 (or <i>tomExtend</i>)</td>
<td>Moves End to the end of the overlapping <i>Unit</i>. Does not move Start.</td>
</tr>
</table>

### -param pDelta

Type: <b>long*</b>

The count of characters that End is moved past. The value of the pointer can be null. On return, the value of
					<i>pDelta</i> is the number of characters the insertion point or End is moved 
					<i>plus</i> 1 if a collapse occurs to the entry End. If the range includes the final CR (carriage return) (at the end of the story) and 
					<i>Extend</i> = tomMove, then
					<i>pDelta</i> is set to 
					–1, to indicate that the collapse occurred 
					<i>before</i> the end of the range (because an insertion point cannot exist beyond the final CR).

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

For comparison, the <a href="/windows/desktop/api/tom/nf-tom-itextrange-startof">ITextRange::StartOf</a> method moves the range ends to the beginning of the first overlapping <i>Unit</i> in the range. Note, the <b>ITextRange::StartOf</b> and <b>ITextRange::EndOf</b> methods differ from the <a href="/windows/desktop/api/tom/nf-tom-itextselection-homekey">HomeKey</a> and <a href="/windows/desktop/api/tom/nf-tom-itextselection-endkey">EndKey</a> methods in that the latter extend from the active end, whereas <b>ITextRange::StartOf</b> extends from Start and <b>ITextRange::EndOf</b> extends from End. If the range is an insertion point on a boundary between <i>Unit</i>s, <b>ITextRange::EndOf</b> does not change End. In particular, calling <b>ITextRange::EndOf</b> (<i>tomCharacter</i>, *, *) does not change End except for an insertion point at the beginning of a story.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-endkey">EndKey</a>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-homekey">HomeKey</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-startof">StartOf</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>