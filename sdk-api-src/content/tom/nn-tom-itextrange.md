---
UID: NN:tom.ITextRange
title: ITextRange (tom.h)
description: The ITextRange objects are powerful editing and data-binding tools that allow a program to select text in a story and then examine or change that text.
helpviewer_keywords: ["ITextRange","ITextRange interface [Windows Controls]","ITextRange interface [Windows Controls]","described","_win32_ITextRange","_win32_ITextRange_cpp","controls.ITextRange","controls._win32_ITextRange","tom/ITextRange"]
old-location: controls\ITextRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextrange.htm
ms.date: 12/05/2018
ms.keywords: ITextRange, ITextRange interface [Windows Controls], ITextRange interface [Windows Controls],described, _win32_ITextRange, _win32_ITextRange_cpp, controls.ITextRange, controls._win32_ITextRange, tom/ITextRange
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
 - ITextRange
 - tom/ITextRange
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
 - ITextRange
---

# ITextRange interface


## -description

The <b>ITextRange</b> objects are powerful editing and data-binding tools that allow a program to select text in a story and then examine or change that text.

## -inheritance

The <b>ITextRange</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITextRange</b> also has these types of members:

## -remarks

Multiple text ranges can be active and work cooperatively on the same story and evolve with the story. For example, if one text range deletes specified text before another text range, the latter tracks the change. In this sense, text ranges are similar to Microsoft Word bookmarks, which also track editing changes. However, bookmarks cannot edit text, while text ranges can. In addition, ranges let you manipulate text without changing the selection or Clipboard, both of which are valuable to end users. The <a href="/windows/desktop/api/tom/nn-tom-itextselection">ITextSelection</a> interface inherits from <b>ITextRange</b> and adds some UI-oriented methods and properties as described in the section on <b>ITextSelection</b>.

You can look at a text range using methods based on character positions. Specifically, a text range is characterized by:

<ul>
<li>The <i>first</i> character position, <i>cpFirst</i>, which points at an insertion point immediately preceding the first character (relative to the beginning of the story) in the range.</li>
<li>The <i>limit</i> position, <i>cpLim</i>, which points at an insertion point immediately following the last character in the range.</li>
</ul>
The first character in a story has <i>cpFirst</i> = zero. If a <i>cp</i> argument has a value greater than the number of characters in the story, the number of characters in the story is used instead. If a <i>cp</i> argument is negative, zero is used instead. For those familiar with Microsoft Visual Basic for Applications, call the <i>cpFirst</i> property <b>Start</b> and the <i>cpLim</i> property <b>End</b> (even though the starting position of a range is also an end).

In the following figure, character positions are represented by the lines separating the letters. The corresponding character position values are given beneath the lines. The range starting at <i>cpFirst</i> = 5 and ending at <i>cpLim</i> = 7 contains the two-letter word is. If this figure depicts the complete text in a story, the story length is 30.

<img alt="Diagram of a 30-character text string, with two of the five words shaded" src="./images/textpos1.png"/>
The <i>length</i> of a range is given by <i>cpLim</i> - <i>cpFirst</i> or equivalently by End - Start. A range with zero length is called a <i>degenerate</i> or <i>empty</i> range and has equal <i>cp</i>* values, that is, <i>cpFirst</i> = <i>cpLim</i>. An example of a degenerate range is the current insertion point. A non-null selection is an example of a nondegenerate range.

Suppose that the range from 5 to 7 indicated by shaded cells in the preceding figure is told to delete its text (see <a href="/windows/desktop/api/tom/nf-tom-itextrange-delete">Delete</a>), thereby turning itself into an insertion point. The range from 25 to 29 would automatically track its contents, namely the word text. The following figure shows the result.

<img alt="Diagram of a 28-character text string, with one of the four words shaded" src="./images/textpos2.png"/>
In this figure, the range for text now has been <i>automatically</i> adjusted to have <i>cpFirst</i> = 23 and <i>cpLim</i> = 27. The owner of the range does not have to worry about updating the range character position values in the face of editing.

The names of the move methods indicate which end to move, but note that if any method attempts to move one range end past the other, both ends get moved to the target position. As a result, the insertion point is at the target position. The concept is that <i>cpFirst</i> and <i>cpLim</i> always have to obey the fundamental condition

0 &lt;= <i>cpFirst</i> &lt;= <i>cpLim</i> &lt;= # characters in story

or equivalently for a range <i>r</i>, 0 &lt;= <i>r</i>.Start &lt;= <i>r</i>.End &lt;= <i>r</i>.StoryLength, which is what you would expect from the names of these quantities.

Another important feature is that all stories contain an undeletable final CR (0xD) character at the end. So even an empty story has a single character, namely the final CR. A range can select this character, but cannot become an insertion point beyond it. To see how this works, try selecting the final CR in a Word document and then press the RIGHT ARROW key to collapse it. The directory tree will collapse before the final CR, but the CR cannot be deleted. The Text Object Model (TOM) functions the same way. So, if <i>r</i>.Start &lt;= <i>r</i>.End, then <i>r</i>.End &lt;= (<i>r</i>.StoryLength – 1). For a discussion about deleting a CR, see <a href="/windows/desktop/api/tom/nf-tom-itextrange-delete">Delete</a>.

Some methods depend on a <i>Unit</i> argument, which can take on the predefined values listed in the following table.

<table class="clsStd">
<tr>
<th>Unit</th>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>tomCharacter</td>
<td>1</td>
<td>Character.</td>
</tr>
<tr>
<td>tomWord</td>
<td>2</td>
<td>Word.</td>
</tr>
<tr>
<td>tomSentence</td>
<td>3</td>
<td>Sentence.</td>
</tr>
<tr>
<td>tomParagraph</td>
<td>4</td>
<td>Paragraph.</td>
</tr>
<tr>
<td>tomLine</td>
<td>5</td>
<td>Line (on display).</td>
</tr>
<tr>
<td>tomStory</td>
<td>6</td>
<td>Story.</td>
</tr>
<tr>
<td>tomScreen</td>
<td>7</td>
<td>Screen (as for PAGE UP/PAGE DOWN).</td>
</tr>
<tr>
<td>tomSection</td>
<td>8</td>
<td>Section.</td>
</tr>
<tr>
<td>tomColumn</td>
<td>9</td>
<td>Table column.</td>
</tr>
<tr>
<td>tomRow</td>
<td>10</td>
<td>Table row.</td>
</tr>
<tr>
<td>tomWindow</td>
<td>11</td>
<td>Upper-left or lower-right of the window.</td>
</tr>
<tr>
<td>tomCell</td>
<td>12</td>
<td>Table cell.</td>
</tr>
<tr>
<td>tomCharFormat</td>
<td>13</td>
<td>Run of constant character formatting.</td>
</tr>
<tr>
<td>tomParaFormat</td>
<td>14</td>
<td>Run of constant paragraph formatting.</td>
</tr>
<tr>
<td>tomTable</td>
<td>15</td>
<td>Table.</td>
</tr>
<tr>
<td>tomObject</td>
<td>16</td>
<td>Embedded object.</td>
</tr>
</table>
 

Most of the <i>Unit</i> values are self-explanatory. However the following descriptions are provided for additional clarity.

<h3><a id="tomWord"></a><a id="tomword"></a><a id="TOMWORD"></a>tomWord</h3>
The tomWord constant is an end of paragraph or a span of alphanumerics or punctuation including any blanks that follow. To get an on-screen feel for tomWord, watch how the caret moves when you press CTRL+RIGHT ARROW (—&gt;) or CTRL+LEFT ARROW (&lt;—) in a Word document.

<h3><a id="tomSentence"></a><a id="tomsentence"></a><a id="TOMSENTENCE"></a>tomSentence</h3>
The tomSentence constant describes a string of text that ends with a period, question mark, or exclamation mark and is followed either by one or more ASCII white space characters (9 through 0xd and 0x20), or the Unicode paragraph separator (0x2029). The trailing white space is part of the sentence. The last sentence in a story does not need to have a period, question mark, or exclamation mark. The start of a story qualifies as the start of a tomSentence, even if the string there does not qualify as a sentence grammatically. Other sentences must follow a sentence end and cannot begin with a period, question mark, or exclamation mark.

<h3><a id="tomParagraph"></a><a id="tomparagraph"></a><a id="TOMPARAGRAPH"></a>tomParagraph</h3>
The tomParagraph constant is a string of text terminated by an end-of-paragraph mark (CRLF, CR, VT (for SHIFT+ENTER), LF, FF, or 0x2029). TOM engines always have an undeletable end-of-paragraph mark at the end of a story. Thus, all TOM stories automatically have at least one tomWord, one tomSentence, and one tomParagraph.

<h3><a id="tomLine"></a><a id="tomline"></a><a id="TOMLINE"></a>tomLine</h3>
The tomLine constant corresponds to one line of text on a display, provided that a display is associated with the range. If no display is associated with a range, tomLine is treated as tomParagraph. A selection automatically has a display and a range that is a duplicate (see <a href="/windows/desktop/api/tom/nf-tom-itextrange-getduplicate">GetDuplicate</a>). Other ranges may not have a display, depending on the TOM engine and context.

Methods that move one or both ends in terms of <i>Unit</i>, such as <a href="/windows/desktop/api/tom/nf-tom-itextrange-move">Move</a>, <a href="/windows/desktop/api/tom/nf-tom-itextrange-moveend">MoveEnd</a>, and <a href="/windows/desktop/api/tom/nf-tom-itextrange-movestart">MoveStart</a>, depend on the signed <i>Count</i> argument. Except for the <a href="/windows/desktop/api/tom/nn-tom-itextselection">ITextSelection</a> geometrical movement commands, if <i>Count</i> is greater than zero, the ends to be moved are moved forward (toward the end of the story), and if <i>Count</i> is less than zero, the ends are moved backward (toward the beginning). The default value of <i>Count</i> for these <b>Move</b> methods is 1. These methods attempt to move <i>Count Units</i>, but movement is never beyond the ends of the story.

Methods that move one or both ends by matching character strings or string patterns, such as <a href="/windows/desktop/api/tom/nf-tom-itextrange-movewhile">MoveWhile</a>, <a href="/windows/desktop/api/tom/nf-tom-itextrange-moveendwhile">MoveEndWhile</a>, and <a href="/windows/desktop/api/tom/nf-tom-itextrange-movestartwhile">MoveStartWhile</a>, can move up to a maximum number of characters given by the signed <i>Count</i> argument. If <i>Count</i> is greater than zero, the ends to be moved are moved forward, and if <i>Count</i> is less than zero, the ends are moved backward. Two special <i>Count</i> values, tomForward and tomBackward, are defined. These values are guaranteed to reach the end and the start of the story, respectively. The default value of <i>Count</i> is tomForward.

In <b>Move</b>* methods that turn a nondegenerate range into a degenerate one, such as <a href="/windows/desktop/api/tom/nf-tom-itextrange-move">Move</a>, <a href="/windows/desktop/api/tom/nf-tom-itextrange-movewhile">MoveWhile</a>, and <a href="/windows/desktop/api/tom/nf-tom-itextrange-moveuntil">MoveUntil</a>, <i>cpFirst</i> is changed if <i>Count</i> is negative and <i>cpLim</i> is changed if <i>Count</i> is positive. After this movement, the other end of the range is also moved to the new location. See the individual methods for more specific <i>Count</i> information. For nondegenerate ranges, the methods <a href="/windows/desktop/api/tom/nf-tom-itextrange-movestart">MoveStart</a>, <a href="/windows/desktop/api/tom/nf-tom-itextrange-moveend">MoveEnd</a>, <a href="/windows/desktop/api/tom/nf-tom-itextrange-movestartwhile">MoveStartWhile</a>, <a href="/windows/desktop/api/tom/nf-tom-itextrange-moveendwhile">MoveEndWhile</a>, <a href="/windows/desktop/api/tom/nf-tom-itextrange-movestartuntil">MoveStartUntil</a> and <a href="/windows/desktop/api/tom/nf-tom-itextrange-moveenduntil">MoveEndUntil</a> move either the starting position (Start) or the ending position (End).

To select a unit that corresponds to a contiguous range, such as a tomWord, tomSentence, and tomParagraph, use the <a href="/windows/desktop/api/tom/nf-tom-itextrange-moveend">MoveEnd</a> method. To select a unit that corresponds to a noncontiguous range, such as tomObject, use the <a href="/windows/desktop/api/tom/nf-tom-itextrange-endof">EndOf</a> method, since the next object may occur after substantial intermediate text, if at all. To select a tomCell unit, the range must be inside a table.

Examples and further explanation of the <i>Count</i> and <i>Unit</i> arguments follow. Note that TOM engines may not support all of the units in the table above. For example, rich edit controls do not offer the concepts of sections, but rather return E_NOTIMPL when given tomSection. However if a TOM engine does support a unit, it has the index value given in the table.

Applications typically do not implement the <b>ITextRange</b> interface. Microsoft text solutions, such as rich edit controls, implement <b>ITextRange</b> as part of their TOM implementation.

Applications can retrieve an <b>ITextRange</b> pointer by calling the <a href="/windows/desktop/api/tom/nf-tom-itextdocument-range">Range</a> method.

## -see-also

<b>Conceptual</b>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>



<a href="/windows/desktop/Controls/using-the-text-object-model">Using The Text Object Model</a>
