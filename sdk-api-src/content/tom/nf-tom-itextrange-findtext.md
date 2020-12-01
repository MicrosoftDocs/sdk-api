---
UID: NF:tom.ITextRange.FindText
title: ITextRange::FindText (tom.h)
description: Searches up to Count characters for the text given by bstr. The starting position and direction are also specified by Count, and the matching criteria are given by Flags.
helpviewer_keywords: ["FindText","FindText method [Windows Controls]","FindText method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","FindText method","ITextRange.FindText","ITextRange::FindText","_win32_ITextRange_FindText","_win32_ITextRange_FindText_cpp","controls.ITextRange_FindText","controls._win32_ITextRange_FindText","tom/ITextRange::FindText"]
old-location: controls\ITextRange_FindText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\findtext.htm
ms.date: 12/05/2018
ms.keywords: FindText, FindText method [Windows Controls], FindText method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],FindText method, ITextRange.FindText, ITextRange::FindText, _win32_ITextRange_FindText, _win32_ITextRange_FindText_cpp, controls.ITextRange_FindText, controls._win32_ITextRange_FindText, tom/ITextRange::FindText
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
 - ITextRange::FindText
 - tom/ITextRange::FindText
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
 - ITextRange.FindText
---

# ITextRange::FindText


## -description

Searches up to <i>Count</i> characters for the text given by <i>bstr</i>. The starting position and direction are also specified by <i>Count</i>, and the matching criteria are given by <i>Flags</i>.

## -parameters

### -param bstr

Type: <b>BSTR</b>

String to find.

### -param Count

Type: <b>long</b>

Maximum number of characters to search. It can be one of the following. 
					

<table class="clsStd">
<tr>
<td><i>tomForward</i></td>
<td>Searches to the end of the story. This is the default value.</td>
</tr>
<tr>
<td><i>n</i> (greater than 0)</td>
<td>Searches forward for <i>n</i> chars, starting from <i>cpFirst.</i> If the range itself matches <i>bstr</i>, another search is attempted from <i>cpFirst</i> + 1.</td>
</tr>
<tr>
<td><i>n</i>(less than 0)</td>
<td>Searches backward for <i>n</i> chars, starting from <i>cpLim. </i>If the range itself matches <i>bstr</i>, another search is attempted from <i>cpLim</i>– 1.</td>
</tr>
<tr>
<td>0 (degenerate range)</td>
<td>Search begins after the range.</td>
</tr>
<tr>
<td>0 (nondegenerate range)</td>
<td>Search is limited to the range.</td>
</tr>
</table>
 

In all cases, if a string is found, the range limits are changed to be those of the matched string and 					<i>pLength</i> is set equal to the length of the string. If the string is not found, the range remains unchanged and <i>pLength</i> is set equal to zero.

### -param Flags

Type: <b>long</b>

Flags governing comparisons. It can be 0 (the default) or any combination of the following values. 
					

<table class="clsStd">
<tr>
<td><i>tomMatchWord</i></td>
<td>2</td>
<td>Matches whole words.</td>
</tr>
<tr>
<td><i>tomMatchCase</i></td>
<td>4</td>
<td>Matches case.</td>
</tr>
<tr>
<td><i>tomMatchPattern</i></td>
<td>8</td>
<td>Matches regular expressions.</td>
</tr>
</table>

### -param pLength

Type: <b>long*</b>

The length of string matched.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns S_FALSE. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

## -remarks

The <b>ITextRange::FindText</b> method can also match special characters by using a caret (^) followed by a special letter. For a list of special characters, see the Special list available in the Microsoft Word 
				<b>Find and Replace</b> dialog box. For example, <code>^p</code> matches the next paragraph mark. Note, <code>^c</code> can be used to represent the Clipboard contents in the string to be replaced. Thus, using <code>^c</code> in the find string enables you to search for rich text. For more details, see the Word Help files. 

As a comparison with the <b>ITextRange::FindText</b> method, the <a href="/windows/desktop/api/tom/nf-tom-itextrange-findtextstart">ITextRange::FindTextStart</a> method searches forward or backward from the range's Start 
				<i>cp</i>, and the <a href="/windows/desktop/api/tom/nf-tom-itextrange-findtextend">ITextRange::FindTextEnd</a> method searches forward or backward from the range's End 
				<i>cp</i>. For more details, see the descriptions of these methods.

The following are several code snippets that show the <b>ITextRange::FindText</b> methods.

Example #1. The following Microsoft Visual Basic for Applications (VBA) program prints all the /* ... */ comments in a story identified by the range r.




```
Sub PrintComments (r As ITextRange)
    r.SetRange 0, 0                                      'r = insertion pt at start of story
    Do While r.FindText("/*") And r.FindTextEnd("*/")    'Select comment
        r.MoveStart tomCharacter, 2                      'But do not include the opening or 
                                                         'closing comment brackets
        r.MoveEnd tomCharacter, -2                       
        Print r                                          'Show the folks
    Loop
End Sub
```


Instead of these comments being printed, they could be inserted into another edit instance and saved to a file, or they could be inserted into separate cells in a table or spreadsheet.

To print all lines containing one or more occurrences of the word "laser", replace the loop by the following code:


```
    While r.FindText("laser")            // Select next occurrence of "laser"
        r.Expand tomLine                // Select enclosing line    
        Print r                    // Print the line
    Wend
```


Example #2. The following program prints a telephone list, given a story that contains an address list. The address list entries are separated by two or more paragraph marks, and each entry has the following form.


```
Person/Business Name
Address (one or more lines)
(area code) telephone number 
```


Note the use of the character <code>^p</code> in the <b>FindText</b> string argument to locate a pair of consecutive paragraph marks.


```
Sub PrintTelephoneList (r As ITextRange)
    r.SetRange 0, 0                 // r = insertion point at start of story
    r.MoveWhile C1_WHITE            // Bypass any initial white space
    Do
        r.EndOf tomParagraph, 1     // Select next para (line): has name
        Print r                    // Print it
        Do
            r.MoveWhile C1_SPACE        // Bypass possible space chars
            If r.Char = Asc("(") Then Exit Do    // Look for start of telephone #
        Loop While r.Move(tomParagraph)    // Go to next paragraph
        r.EndOf tomParagraph, 1        // Select line with telephone number
        Print r                    // Print it
    Loop While r.FindText("^p^p")        // Find two consecutive para marks
End Sub
```


Example #3. The following subroutine replaces all occurrences of the string, str1, in a range by str2:


```
Sub Replace ( tr As ITextRange, str1 As String, str2 As String )
    Dim r As ITextRange
    r = tr.Duplicate                // Copy tr parameters to r
    r.End = r.Start                    // Convert to insertion point at Start
    While r.FindText(str1, tr.End - r.End)        // Match next occurrence of str
        r = str2                // Replace it with rep
    Wend                        // Iterate till no more matches
End Sub
```


Example #4. The following line of code inserts a blank before the first occurrence of a right parenthesis, "(", that follows an occurrence of HRESULT. 


```
    If r.FindText("HRESULT") And r.FindText("(") Then r = " ("
```


To do this for all such occurrences, change the If into a While/Wend loop in the above line of code. This an example of a <b>FIND/REPLACE</b> macro that cannot be run with <b>Find and Replace</b> dialog boxes.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-findtextend">FindTextEnd</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-findtextstart">FindTextStart</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>