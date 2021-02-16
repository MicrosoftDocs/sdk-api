---
UID: NF:tom.ITextRange.Move
title: ITextRange::Move (tom.h)
description: Moves the insertion point forward or backward a specified number of units. If the range is nondegenerate, the range is collapsed to an insertion point at either end, depending on Count, and then is moved.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","Move method","ITextRange.Move","ITextRange::Move","Move","Move method [Windows Controls]","Move method [Windows Controls]","ITextRange interface","_win32_ITextRange_Move","_win32_ITextRange_Move_cpp","controls.ITextRange_Move","controls._win32_ITextRange_Move","tom/ITextRange::Move"]
old-location: controls\ITextRange_Move.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\move.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],Move method, ITextRange.Move, ITextRange::Move, Move, Move method [Windows Controls], Move method [Windows Controls],ITextRange interface, _win32_ITextRange_Move, _win32_ITextRange_Move_cpp, controls.ITextRange_Move, controls._win32_ITextRange_Move, tom/ITextRange::Move
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
 - ITextRange::Move
 - tom/ITextRange::Move
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
 - ITextRange.Move
---

# ITextRange::Move


## -description

Moves the insertion point forward or backward a specified number of units. If the range is nondegenerate, the range is collapsed to an insertion point at either end, depending on <i>Count</i>, and then is moved.

## -parameters

### -param Unit

Type: <b>long</b>

Unit to use. The default value is <b>tomCharacter</b>. For information on other values, see the discussion in <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>.

### -param Count

Type: <b>long</b>

Number of <i>Unit</i>s to move past. The default value is 1. If <i>Count</i> is greater than zero, motion is forward—toward the end of the story—and if <i>Count</i> is less than zero, motion is backward—toward the beginning. If <i>Count</i> is zero, the range is unchanged.

### -param pDelta

Type: <b>long*</b>

The actual number of <i>Unit</i>s the insertion point moves past. The pointer can be <b>NULL</b>. For more information, see the Remarks section.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds in moving the insertion point, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
<i>Unit</i> is not supported.

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

If the range is degenerate (an insertion point), this method tries to move the insertion point <i>Count</i> <i>Unit</i>s. 

If the range is nondegenerate and <i>Count</i> is greater than zero, this method collapses the range at the end character position, moves the resulting insertion point forward to a <i>Unit</i> boundary (if it is not already at one), and then tries to move <i>Count</i> - 1 <i>Unit</i>s forward. If the range is nondegenerate and <i>Count</i> is less than zero, this method collapses the range at the start character position, moves the resulting insertion point backward to a <i>Unit</i> boundary (if it isn't already at one), and then tries to move |<i>Count</i>| - 1 <i>Unit</i>s backward. Thus, in both cases, collapsing a nondegenerate range to an insertion point, whether moving to the start or end of the <i>Unit</i> following the collapse, counts as a <i>Unit</i>.

The <b>ITextRange::Move</b> method returns <i>pDelta</i> = number of <i>Unit</i>s actually moved. This method never moves the insertion point beyond the story of this range. If <i>Count</i><i>Unit</i>s would move the insertion point before the beginning of the story, it is moved to the story beginning and <i>pDelta</i> is set accordingly. Similarly, if <i>Count</i> 
				<i>Unit</i>s would move it beyond the end of the story, it is moved to the story end.

The <b>ITextRange::Move</b> method works similarly to the UI-oriented <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveleft">MoveLeft</a> and <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveright">MoveRight</a> methods, except that the direction of motion is logical rather than geometrical. That is, with <b>ITextRange::Move</b> the direction is either toward the end or toward the start of the story. Depending on the language, moving toward the end of the story could be moving to the left or to the right. To get a feel for <i>Count</i>, press Ctrl+Right Arrow in a Microsoft Word document for a variety of selections. In left-to-right text, this keystroke behaves the same as <code>Move(tomWord, 1)</code>, and <code>MoveRight(tomWord, 1)</code>. <i>Count</i> corresponds to the number of times you press Ctrl+Right Arrow.

For example, if you press Ctrl+Right Arrow for the selections shown in both of the following figures, you end up with an insertion point at character position 8, since this command collapses the selections at their end character positions (7 and 8, respectively) and moves to the next <b>tomWord</b> boundary.

<img alt="Character positions for text string" src="./images/textpos3.png"/>
<img alt="Character positions for text string" src="./images/textpos3.png"/>
The first selection does not include the blank space at character position 7, so Ctrl+Right Arrow moves past the space to the <b>tomWord</b> boundary at character position 8. The end character position is already at a <b>tomWord</b> boundary for the second selection, so Ctrl+Right Arrow just collapses the selection at that boundary. Similarly, Ctrl+Left Arrow, which for this text acts like <code>Move(tomWord, -1)</code>, and <code>MoveLeft(tomWord, 1)</code> collapses the first selection at character position 5, which is already at a <b>tomWord</b> boundary, so no more motion occurs. But Ctrl+Left Arrow collapses the second selection at character position 4 and then moves to zero, since that's the next <b>tomWord</b> boundary in the direction of motion.

The return argument, <i>pDelta</i>, is set equal to the number of <i>Unit</i>s that the insertion point is moved including one <i>Unit</i> for collapsing a nondegenerate range and moving it to a <i>Unit</i> boundary. So, if no motion and no collapse occur, as when the range is an insertion point at the end of the story, <i>pDelta</i> is set equal to zero. This approach is useful for controlling program loops that process a whole story.

In both of the cases mentioned above, calling <code>Move(tomWord, 1)</code> sets <i>pDelta</i> equal to 1 because the ranges were collapsed. Similarly, calling <code>Move(tomWord, -1)</code> sets <i>pDelta</i> equal to -1 for both cases. Collapsing, with or without moving part of a <i>Unit</i> to a <i>Unit</i> boundary, counts as a <i>Unit</i> moved.

The direction of motion refers to the logical character ordering in the plain-text backing store. This approach avoids the problems of geometrical ordering, such as left versus right and up versus down, in international software. Such geometrical methods are still needed in the edit engine, of course, since keyboards have arrow keys to invoke them. If the range is really an <a href="/windows/desktop/api/tom/nn-tom-itextselection">ITextSelection</a> object, then methods like <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveleft">MoveLeft</a> and <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveright">MoveRight</a> can be used.

If <i>Unit</i> specifies characters (<b>tomCharacter</b>), the Text Object Model (TOM) uses the Unicode character set. To convert between Unicode and multibyte character sets the <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a> functions provide easy ways to convert between Unicode and multibyte character sets on import and export, respectively. For more information, see <a href="/windows/desktop/api/tom/nf-tom-itextdocument-open">Open</a>. In this connection, the use of a carriage return/line feed (CR/LF) to separate paragraphs is as problematic as double-byte character set (DBCS). The <a href="/windows/desktop/api/tom/nn-tom-itextselection">ITextSelection</a> UI methods back up over a CR/LF as if it were a single character, but the <b>ITextRange::Move</b> methods count CR/LFs as two characters. It's clearly better to use a single character as a paragraph separator, which in TOM is represented by a character return, although the Unicode paragraph separator character, 0x2029, is accepted. In general, TOM engines should support CR/LF, carriage return (CR), line feed (LF), vertical tab, form feed, and 0x2029. Microsoft Rich Edit 2.0 also supports CR/CR/LF for backward compatibility.

See also the <a href="/windows/desktop/api/tom/nf-tom-itextrange-movestart">ITextRange::MoveStart</a> and <a href="/windows/desktop/api/tom/nf-tom-itextrange-moveend">ITextRange::MoveEnd</a> methods, which move the range Start or End position <i>Count</i> 
				<i>Unit</i>s, respectively.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-moveend">MoveEnd</a>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-moveleft">MoveLeft</a>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-moveright">MoveRight</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-movestart">MoveStart</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument-open">Open</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a>