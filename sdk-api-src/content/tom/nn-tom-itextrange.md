---
UID: NN:tom.ITextRange
title: ITextRange
author: windows-sdk-content
description: The ITextRange objects are powerful editing and data-binding tools that allow a program to select text in a story and then examine or change that text.
old-location: controls\ITextRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextrange.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ITextRange, ITextRange interface [Windows Controls], ITextRange interface [Windows Controls],described, _win32_ITextRange, _win32_ITextRange_cpp, controls.ITextRange, controls._win32_ITextRange, tom/ITextRange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange interface


## -description


The <b>ITextRange</b> objects are powerful editing and data-binding tools that allow a program to select text in a story and then examine or change that text.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextRange</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITextRange</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextRange</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787732(v=VS.85).aspx">CanEdit</a>
</td>
<td align="left" width="63%">
Determines whether the specified range can be edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787734(v=VS.85).aspx">CanPaste</a>
</td>
<td align="left" width="63%">
Determines if a data object can be pasted, using a specified format, into the current range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787736(v=VS.85).aspx">ChangeCase</a>
</td>
<td align="left" width="63%">
Changes the case of letters in this range according to the 
			<i>Type</i> parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787740(v=VS.85).aspx">Collapse</a>
</td>
<td align="left" width="63%">
Collapses the specified text range into a degenerate point at either the beginning or end of the range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787742(v=VS.85).aspx">Copy</a>
</td>
<td align="left" width="63%">
Copies the text to a data object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787744(v=VS.85).aspx">Cut</a>
</td>
<td align="left" width="63%">
Cuts the plain or rich text to a data object or to the Clipboard, depending on the 
			<i>pVar</i> parameter. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787746(v=VS.85).aspx">Delete</a>
</td>
<td align="left" width="63%">
Mimics the DELETE and BACKSPACE keys, with and without the CTRL key depressed. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787769(v=VS.85).aspx">EndOf</a>
</td>
<td align="left" width="63%">
Moves this range's ends to the end of the last overlapping <i>Unit</i> in the range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787781(v=VS.85).aspx">Expand</a>
</td>
<td align="left" width="63%">
Expands this range so that any partial units it contains are completely contained. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787783(v=VS.85).aspx">FindText</a>
</td>
<td align="left" width="63%">
Searches up to <i>Count</i> characters for the text given by <i>bstr</i>. The starting position and direction are also specified by <i>Count</i>, and the matching criteria are given by <i>Flags</i>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773921(v=VS.85).aspx">FindTextEnd</a>
</td>
<td align="left" width="63%">
Searches up to <i>Count</i> characters for the string, <i>bstr</i>, starting from the range's End <i>cp</i>. The search is subject to the comparison parameter, <i>Flags</i>. If the string is found, the End <i>cp</i> is changed to be the end of the matched string, and <i>pLength</i> is set equal to the length of the string. If the string is not found, the range is unchanged and <i>pLength</i> is set equal to zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773923(v=VS.85).aspx">FindTextStart</a>
</td>
<td align="left" width="63%">
Searches up to <i>Count</i> characters for the string, <i>bstr</i>, starting at the range's Start 

			<i>cp</i> (<i>cpFirst)</i>. The search is subject to the comparison parameter, <i>Flags</i>. If the string is found, the Start 
			<i>cp</i> is changed to the matched string, and <i>pLength</i> is set equal to the length of the string. If the string is not found, the range is unchanged, and <i>pLength</i> is set equal to zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773937(v=VS.85).aspx">GetChar</a>
</td>
<td align="left" width="63%">
Gets the character at the start position of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787840(v=VS.85).aspx">GetDuplicate</a>
</td>
<td align="left" width="63%">
Gets a duplicate of this range object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773943(v=VS.85).aspx">GetEmbeddedObject</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the embedded object at the start of the specified range, that is, at <i>cpFirst</i>. The range must either be an insertion point or it must select only the embedded object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773947(v=VS.85).aspx">GetEnd</a>
</td>
<td align="left" width="63%">
Gets the end character position of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773955(v=VS.85).aspx">GetFont</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a> object with the character attributes of the specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773958(v=VS.85).aspx">GetFormattedText</a>
</td>
<td align="left" width="63%">
Gets an <b>ITextRange</b> object with the specified range's formatted text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773964(v=VS.85).aspx">GetIndex</a>
</td>
<td align="left" width="63%">
Retrieves the story index of the <i>Unit</i> parameter at the specified range Start character position. The first <i>Unit</i> in a story has an index value of 1. The index of a <i>Unit</i> is the same for all character positions from that immediately preceding the <i>Unit</i> up to the last character in the <i>Unit</i>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774001(v=VS.85).aspx">GetPara</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/en-us/library/Bb774056(v=VS.85).aspx">ITextPara</a> object with the paragraph attributes of the specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774003(v=VS.85).aspx">GetPoint</a>
</td>
<td align="left" width="63%">
Retrieves screen coordinates for the start or end character position in the text range, along with the intra-line position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774026(v=VS.85).aspx">GetStart</a>
</td>
<td align="left" width="63%">
Gets the start character position of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774028(v=VS.85).aspx">GetStoryLength</a>
</td>
<td align="left" width="63%">
Gets the count of characters in the range's story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774030(v=VS.85).aspx">GetStoryType</a>
</td>
<td align="left" width="63%">
Get the type of the range's story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774036(v=VS.85).aspx">GetText</a>
</td>
<td align="left" width="63%">
Gets the plain text in this range. The Text property is the default property of the <b>ITextRange</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774046(v=VS.85).aspx">InRange</a>
</td>
<td align="left" width="63%">
Determines whether this range is within or at the same text as a specified range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774048(v=VS.85).aspx">InStory</a>
</td>
<td align="left" width="63%">
Determines whether this range's story is the same as a specified range's story. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787841(v=VS.85).aspx">IsEqual</a>
</td>
<td align="left" width="63%">
Determines whether this range has the same character positions and story as those of a specified range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774064(v=VS.85).aspx">Move</a>
</td>
<td align="left" width="63%">
Moves the insertion point forward or backward a specified number of units. If the range is nondegenerate, the range is collapsed to an insertion point at either end, depending on <i>Count</i>, and then is moved. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774068(v=VS.85).aspx">MoveEnd</a>
</td>
<td align="left" width="63%">
Moves the end position of the range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774070(v=VS.85).aspx">MoveEndUntil</a>
</td>
<td align="left" width="63%">
Moves the range's end to the character position of the first character found that is in the set of characters specified by <i>Cset</i>, provided that the character is found within <i>Count</i> characters of the range's end.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774072(v=VS.85).aspx">MoveEndWhile</a>
</td>
<td align="left" width="63%">
Moves the end of the range either <i>Count</i> characters or just past all contiguous characters that are found in the set of characters specified by <i>Cset</i>, whichever is less. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774078(v=VS.85).aspx">MoveStart</a>
</td>
<td align="left" width="63%">
Moves the start postion of the range the specified number of units in the specified direction. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774080(v=VS.85).aspx">MoveStartUntil</a>
</td>
<td align="left" width="63%">
Moves the start position of the range the position of the first character found that is in the set of characters specified by <i>Cset</i>, provided that the character is found within <i>Count</i> characters of the start position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774082(v=VS.85).aspx">MoveStartWhile</a>
</td>
<td align="left" width="63%">
Moves the start position of the range either <i>Count</i> characters, or just past all contiguous characters that are found in the set of characters specified by <i>Cset</i>, whichever is less. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774084(v=VS.85).aspx">MoveUntil</a>
</td>
<td align="left" width="63%">
Searches up to <i>Count</i> characters for the first character in the set of characters specified by <i>Cset</i>. If a character is found, the range is collapsed to that point. The start of the search and the direction are also specified by <i>Count</i>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774088(v=VS.85).aspx">MoveWhile</a>
</td>
<td align="left" width="63%">
Starts at a specified end of a range and searches while the characters belong to the set specified by <i>Cset</i> and while the number of characters is less than or equal to <i>Count</i>. The range is collapsed to an insertion point when a non-matching character is found.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774095(v=VS.85).aspx">Paste</a>
</td>
<td align="left" width="63%">
Pastes text from a specified data object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774119(v=VS.85).aspx">ScrollIntoView</a>
</td>
<td align="left" width="63%">
Scrolls the specified range into view. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774121(v=VS.85).aspx">Select</a>
</td>
<td align="left" width="63%">
Sets the start and end positions, and story values of the active selection, to those of this range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774133(v=VS.85).aspx">SetChar</a>
</td>
<td align="left" width="63%">
Sets the character at the starting position of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774139(v=VS.85).aspx">SetEnd</a>
</td>
<td align="left" width="63%">
Sets the end position of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774145(v=VS.85).aspx">SetFont</a>
</td>
<td align="left" width="63%">
Sets this range's character attributes to those of the specified <a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774149(v=VS.85).aspx">SetFormattedText</a>
</td>
<td align="left" width="63%">
Sets the formatted text of this range text to the formatted text of the specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774157(v=VS.85).aspx">SetIndex</a>
</td>
<td align="left" width="63%">
Changes this range to the specified unit of the story. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787797(v=VS.85).aspx">SetPara</a>
</td>
<td align="left" width="63%">
Sets the paragraph attributes of this range to those of the specified <a href="https://msdn.microsoft.com/en-us/library/Bb774056(v=VS.85).aspx">ITextPara</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787799(v=VS.85).aspx">SetPoint</a>
</td>
<td align="left" width="63%">
Changes the range based on a specified point at or up through (depending on <i>Extend</i>) the point (<i>x</i>, <i>y</i>) aligned according to <i>Type</i>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787805(v=VS.85).aspx">SetRange</a>
</td>
<td align="left" width="63%">
Adjusts the range endpoints to the specified values. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787823(v=VS.85).aspx">SetStart</a>
</td>
<td align="left" width="63%">
Sets the character  position for the start of this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787831(v=VS.85).aspx">SetText</a>
</td>
<td align="left" width="63%">
Sets the text in this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787835(v=VS.85).aspx">StartOf</a>
</td>
<td align="left" width="63%">
Moves the range ends to the start of the first overlapping <i>Unit</i> in the range. 

</td>
</tr>
</table> 


## -remarks



Multiple text ranges can be active and work cooperatively on the same story and evolve with the story. For example, if one text range deletes specified text before another text range, the latter tracks the change. In this sense, text ranges are similar to Microsoft Word bookmarks, which also track editing changes. However, bookmarks cannot edit text, while text ranges can. In addition, ranges let you manipulate text without changing the selection or Clipboard, both of which are valuable to end users. The <a href="https://msdn.microsoft.com/en-us/library/Bb774060(v=VS.85).aspx">ITextSelection</a> interface inherits from <b>ITextRange</b> and adds some UI-oriented methods and properties as described in the section on <b>ITextSelection</b>.

You can look at a text range using methods based on character positions. Specifically, a text range is characterized by:

<ul>
<li>The <i>first</i> character position, <i>cpFirst</i>, which points at an insertion point immediately preceding the first character (relative to the beginning of the story) in the range.</li>
<li>The <i>limit</i> position, <i>cpLim</i>, which points at an insertion point immediately following the last character in the range.</li>
</ul>
The first character in a story has <i>cpFirst</i> = zero. If a <i>cp</i> argument has a value greater than the number of characters in the story, the number of characters in the story is used instead. If a <i>cp</i> argument is negative, zero is used instead. For those familiar with Microsoft Visual Basic for Applications, call the <i>cpFirst</i> property <b>Start</b> and the <i>cpLim</i> property <b>End</b> (even though the starting position of a range is also an end).

In the following figure, character positions are represented by the lines separating the letters. The corresponding character position values are given beneath the lines. The range starting at <i>cpFirst</i> = 5 and ending at <i>cpLim</i> = 7 contains the two-letter word is. If this figure depicts the complete text in a story, the story length is 30.

<img alt="Diagram of a 30-character text string, with two of the five words shaded" src="./images/textpos1.png"/>
The <i>length</i> of a range is given by <i>cpLim</i> - <i>cpFirst</i> or equivalently by End - Start. A range with zero length is called a <i>degenerate</i> or <i>empty</i> range and has equal <i>cp</i>* values, that is, <i>cpFirst</i> = <i>cpLim</i>. An example of a degenerate range is the current insertion point. A non-null selection is an example of a nondegenerate range.

Suppose that the range from 5 to 7 indicated by shaded cells in the preceding figure is told to delete its text (see <a href="https://msdn.microsoft.com/en-us/library/Bb787746(v=VS.85).aspx">Delete</a>), thereby turning itself into an insertion point. The range from 25 to 29 would automatically track its contents, namely the word text. The following figure shows the result.

<img alt="Diagram of a 28-character text string, with one of the four words shaded" src="./images/textpos2.png"/>
In this figure, the range for text now has been <i>automatically</i> adjusted to have <i>cpFirst</i> = 23 and <i>cpLim</i> = 27. The owner of the range does not have to worry about updating the range character position values in the face of editing.

The names of the move methods indicate which end to move, but note that if any method attempts to move one range end past the other, both ends get moved to the target position. As a result, the insertion point is at the target position. The concept is that <i>cpFirst</i> and <i>cpLim</i> always have to obey the fundamental condition

0 &lt;= <i>cpFirst</i> &lt;= <i>cpLim</i> &lt;= # characters in story

or equivalently for a range <i>r</i>, 0 &lt;= <i>r</i>.Start &lt;= <i>r</i>.End &lt;= <i>r</i>.StoryLength, which is what you would expect from the names of these quantities.

Another important feature is that all stories contain an undeletable final CR (0xD) character at the end. So even an empty story has a single character, namely the final CR. A range can select this character, but cannot become an insertion point beyond it. To see how this works, try selecting the final CR in a Word document and then press the RIGHT ARROW key to collapse it. The directory tree will collapse before the final CR, but the CR cannot be deleted. The Text Object Model (TOM) functions the same way. So, if <i>r</i>.Start &lt;= <i>r</i>.End, then <i>r</i>.End &lt;= (<i>r</i>.StoryLength – 1). For a discussion about deleting a CR, see <a href="https://msdn.microsoft.com/en-us/library/Bb787746(v=VS.85).aspx">Delete</a>.

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
The tomLine constant corresponds to one line of text on a display, provided that a display is associated with the range. If no display is associated with a range, tomLine is treated as tomParagraph. A selection automatically has a display and a range that is a duplicate (see <a href="https://msdn.microsoft.com/en-us/library/Bb787840(v=VS.85).aspx">GetDuplicate</a>). Other ranges may not have a display, depending on the TOM engine and context.

Methods that move one or both ends in terms of <i>Unit</i>, such as <a href="https://msdn.microsoft.com/en-us/library/Bb774064(v=VS.85).aspx">Move</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb774068(v=VS.85).aspx">MoveEnd</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb774078(v=VS.85).aspx">MoveStart</a>, depend on the signed <i>Count</i> argument. Except for the <a href="https://msdn.microsoft.com/en-us/library/Bb774060(v=VS.85).aspx">ITextSelection</a> geometrical movement commands, if <i>Count</i> is greater than zero, the ends to be moved are moved forward (toward the end of the story), and if <i>Count</i> is less than zero, the ends are moved backward (toward the beginning). The default value of <i>Count</i> for these <b>Move</b> methods is 1. These methods attempt to move <i>Count Units</i>, but movement is never beyond the ends of the story.

Methods that move one or both ends by matching character strings or string patterns, such as <a href="https://msdn.microsoft.com/en-us/library/Bb774088(v=VS.85).aspx">MoveWhile</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb774072(v=VS.85).aspx">MoveEndWhile</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb774082(v=VS.85).aspx">MoveStartWhile</a>, can move up to a maximum number of characters given by the signed <i>Count</i> argument. If <i>Count</i> is greater than zero, the ends to be moved are moved forward, and if <i>Count</i> is less than zero, the ends are moved backward. Two special <i>Count</i> values, tomForward and tomBackward, are defined. These values are guaranteed to reach the end and the start of the story, respectively. The default value of <i>Count</i> is tomForward.

In <b>Move</b>* methods that turn a nondegenerate range into a degenerate one, such as <a href="https://msdn.microsoft.com/en-us/library/Bb774064(v=VS.85).aspx">Move</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb774088(v=VS.85).aspx">MoveWhile</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb774084(v=VS.85).aspx">MoveUntil</a>, <i>cpFirst</i> is changed if <i>Count</i> is negative and <i>cpLim</i> is changed if <i>Count</i> is positive. After this movement, the other end of the range is also moved to the new location. See the individual methods for more specific <i>Count</i> information. For nondegenerate ranges, the methods <a href="https://msdn.microsoft.com/en-us/library/Bb774078(v=VS.85).aspx">MoveStart</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb774068(v=VS.85).aspx">MoveEnd</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb774082(v=VS.85).aspx">MoveStartWhile</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb774072(v=VS.85).aspx">MoveEndWhile</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb774080(v=VS.85).aspx">MoveStartUntil</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb774070(v=VS.85).aspx">MoveEndUntil</a> move either the starting position (Start) or the ending position (End).

To select a unit that corresponds to a contiguous range, such as a tomWord, tomSentence, and tomParagraph, use the <a href="https://msdn.microsoft.com/en-us/library/Bb774068(v=VS.85).aspx">MoveEnd</a> method. To select a unit that corresponds to a noncontiguous range, such as tomObject, use the <a href="https://msdn.microsoft.com/en-us/library/Bb787769(v=VS.85).aspx">EndOf</a> method, since the next object may occur after substantial intermediate text, if at all. To select a tomCell unit, the range must be inside a table.

Examples and further explanation of the <i>Count</i> and <i>Unit</i> arguments follow. Note that TOM engines may not support all of the units in the table above. For example, rich edit controls do not offer the concepts of sections, but rather return E_NOTIMPL when given tomSection. However if a TOM engine does support a unit, it has the index value given in the table.

Applications typically do not implement the <b>ITextRange</b> interface. Microsoft text solutions, such as rich edit controls, implement <b>ITextRange</b> as part of their TOM implementation.

Applications can retrieve an <b>ITextRange</b> pointer by calling the <a href="https://msdn.microsoft.com/en-us/library/Bb774097(v=VS.85).aspx">Range</a> method.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787726(v=VS.85).aspx">Using The Text Object Model</a>
 

 

