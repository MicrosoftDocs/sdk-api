---
UID: NF:tom.ITextRange.MoveEndUntil
title: ITextRange::MoveEndUntil (tom.h)
description: Moves the range's end to the character position of the first character found that is in the set of characters specified by Cset, provided that the character is found within Count characters of the range's end.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","MoveEndUntil method","ITextRange.MoveEndUntil","ITextRange::MoveEndUntil","MoveEndUntil","MoveEndUntil method [Windows Controls]","MoveEndUntil method [Windows Controls]","ITextRange interface","_win32_ITextRange_MoveEndUntil","_win32_ITextRange_MoveEndUntil_cpp","controls.ITextRange_MoveEndUntil","controls._win32_ITextRange_MoveEndUntil","tom/ITextRange::MoveEndUntil"]
old-location: controls\ITextRange_MoveEndUntil.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\moveenduntil.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],MoveEndUntil method, ITextRange.MoveEndUntil, ITextRange::MoveEndUntil, MoveEndUntil, MoveEndUntil method [Windows Controls], MoveEndUntil method [Windows Controls],ITextRange interface, _win32_ITextRange_MoveEndUntil, _win32_ITextRange_MoveEndUntil_cpp, controls.ITextRange_MoveEndUntil, controls._win32_ITextRange_MoveEndUntil, tom/ITextRange::MoveEndUntil
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
 - ITextRange::MoveEndUntil
 - tom/ITextRange::MoveEndUntil
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
 - ITextRange.MoveEndUntil
---

# ITextRange::MoveEndUntil


## -description

Moves the range's end to the character position of the first character found that is in the set of characters specified by <i>Cset</i>, provided that the character is found within <i>Count</i> characters of the range's end.

## -parameters

### -param Cset

Type: <b>VARIANT*</b>

The character set to use in the match. This could be an explicit string of characters or a character-set index. For more information, see <a href="/windows/desktop/Controls/about-text-object-model">Character Match Sets</a>.

### -param Count

Type: <b>long</b>

Maximum number of characters to move past. The default value is <b>tomForward</b>, which searches to the end of the story. If <i>Count</i> is greater than zero, the search moves forward (toward the end of the story). If <i>Count</i> is less than zero, the search moves backward (toward the beginning of the story). If  <i>Count</i> is zero, the end position is unchanged.

### -param pDelta

Type: <b>long*</b>

The actual number of characters that the range end is moved, plus 1 for a match if <i>Count</i> is greater than zero, and –1 for a match if <i>Count</i> is less than zero. The value can be null.

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
<dt><b>Value</b></dt>
</dl>
</td>
<td width="60%">
Meaning

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Cset is invalid.

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

If no character from the set specified by <i>Cset</i> is found within <i>Count</i> positions of the range's end, the range is left unchanged. If the new end precedes the old start, the new start is set equal to the new end.

The motion described by <b>ITextRange::MoveEndUntil</b> is logical rather than geometric. That is, motion is toward the end or toward the start of a story. Depending on the language, moving to the end of the story could be moving left or moving right. 

For more information, see <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> and <a href="/windows/desktop/api/tom/nf-tom-itextrange-move">ITextRange::Move</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-move">Move</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-moveuntil">MoveUntil</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>