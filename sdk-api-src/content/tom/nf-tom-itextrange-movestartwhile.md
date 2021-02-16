---
UID: NF:tom.ITextRange.MoveStartWhile
title: ITextRange::MoveStartWhile (tom.h)
description: Moves the start position of the range either Count characters, or just past all contiguous characters that are found in the set of characters specified by Cset, whichever is less.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","MoveStartWhile method","ITextRange.MoveStartWhile","ITextRange::MoveStartWhile","MoveStartWhile","MoveStartWhile method [Windows Controls]","MoveStartWhile method [Windows Controls]","ITextRange interface","_win32_ITextRange_MoveStartWhile","_win32_ITextRange_MoveStartWhile_cpp","controls.ITextRange_MoveStartWhile","controls._win32_ITextRange_MoveStartWhile","tom/ITextRange::MoveStartWhile"]
old-location: controls\ITextRange_MoveStartWhile.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\movestartwhile.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],MoveStartWhile method, ITextRange.MoveStartWhile, ITextRange::MoveStartWhile, MoveStartWhile, MoveStartWhile method [Windows Controls], MoveStartWhile method [Windows Controls],ITextRange interface, _win32_ITextRange_MoveStartWhile, _win32_ITextRange_MoveStartWhile_cpp, controls.ITextRange_MoveStartWhile, controls._win32_ITextRange_MoveStartWhile, tom/ITextRange::MoveStartWhile
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
 - ITextRange::MoveStartWhile
 - tom/ITextRange::MoveStartWhile
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
 - ITextRange.MoveStartWhile
---

# ITextRange::MoveStartWhile


## -description

Moves the start position of the range either <i>Count</i> characters, or just past all contiguous characters that are found in the set of characters specified by <i>Cset</i>, whichever is less.

## -parameters

### -param Cset

Type: <b>VARIANT*</b>

The character set to use in the match. This could be an explicit string of characters or a character-set index. For more information, see <a href="/windows/desktop/Controls/about-text-object-model">Character Match Sets</a>.

### -param Count

Type: <b>long</b>

Maximum number of characters to move past. The default value is <b>tomForward</b>, which searches to the end of the story. If <i>Count</i> is greater than zero, the search is forward—toward the end of the story—and if <i>Count</i> is less than zero, search is backward—toward the beginning. If  <i>Count</i> is zero, the start position is unchanged.

### -param pDelta

Type: <b>long*</b>

The actual count of characters that the start position is moved. This parameter can be null.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Cset is not valid.

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

If the new start follows the old end, the new end is set equal to the new start.

The motion described by <b>ITextRange::MoveStartWhile</b> is logical rather than geometric. That is, motion is toward the end or toward the start of a story. Depending on the language, moving to the end of the story could be moving left or moving right. 

For more information, see <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> and <a href="/windows/desktop/api/tom/nf-tom-itextrange-move">ITextRange::Move</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-move">Move</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-movewhile">MoveWhile</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>