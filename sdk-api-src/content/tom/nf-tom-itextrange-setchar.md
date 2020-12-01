---
UID: NF:tom.ITextRange.SetChar
title: ITextRange::SetChar (tom.h)
description: Sets the character at the starting position of the range.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","SetChar method","ITextRange.SetChar","ITextRange::SetChar","SetChar","SetChar method [Windows Controls]","SetChar method [Windows Controls]","ITextRange interface","_win32_ITextRange_SetChar","_win32_ITextRange_SetChar_cpp","controls.ITextRange_SetChar","controls._win32_ITextRange_SetChar","tom/ITextRange::SetChar"]
old-location: controls\ITextRange_SetChar.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setchar.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],SetChar method, ITextRange.SetChar, ITextRange::SetChar, SetChar, SetChar method [Windows Controls], SetChar method [Windows Controls],ITextRange interface, _win32_ITextRange_SetChar, _win32_ITextRange_SetChar_cpp, controls.ITextRange_SetChar, controls._win32_ITextRange_SetChar, tom/ITextRange::SetChar
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
 - ITextRange::SetChar
 - tom/ITextRange::SetChar
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
 - ITextRange.SetChar
---

# ITextRange::SetChar


## -description

Sets the character at the starting position of the range.

## -parameters

### -param Char

Type: <b>long</b>

New value for character at the starting position.

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Text is write-protected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -remarks

<b>ITextRange::SetChar</b> lets you specify the precise character code to use. However, string literals with similar looking glyphs can be misleading. 

The characters set by this method are <b>LONG</b> instead of a <b>BSTR</b>. This hides the way that they are stored in the backing store, (as bytes, words, variable-length, and so forth). 

Frequently on systems that do not have automatic word-wrapping, documents have hard carriage returns inserted just for line breaks. The following code shows a simple, but not perfect, way to convert such hard carriage returns back to blanks for the story that is associated with the range r. 




```
    Sub EnableWrap(r As ITextRange)   // Convert false hard CRs to soft
        r.SetRange 0, 0               // r is set at start of story
        While r.Move(tomParagraph)    // Go to start of next paragraph
            If r.MoveWhile(C1_WHITE, 1) = 0 Then    // Next char isn't white space
                r.Move tomCharacter, -1
                r.SetChar = Asc(" ")    // Replace CR by blank
            End If
        Wend        // Loop till no more CRs in story
    End Sub
```


Alternatively, you could use the following inside the IF loop.


```
r.MoveStart tomCharacter, -1        // Select previous char (the CR)
r = " "        // Replace it with a blank
```


This approach enables you to wrap the text to other widths. However, the algorithm isn't perfect: it assumes that a hard carriage return that is followed by anything other than white space (blank, tab, line feed, carriage return, and so forth) should be replaced by a blank. The algorithm also assumes that the carriage return character is a single character like carriage return  or the Unicode end-of-paragraph (EOP) 0x2029 character. And, the combination carriage return and line feed isn't matched and would require writing and executing more code (or use <code>FindText(^p)</code>). Another caution is that there are other cases, such as mixed code and documentation, where the algorithm does not work correctly. 

However, <b>ITextRange::SetChar</b> is more efficient than a replace operation that is accomplished by a delete followed by an insertion. Thus, rewriting the code without using <b>ITextRange::SetChar</b> would probably be much slower. 

The <i>Char</i> property, which can do most things that a characters collection can, has two big advantages: it can reference any character in the parent story instead of being limited to the parent range, and it's significantly faster, since <b>LONG</b>s rather than range objects are involved. Because of these advantages, the Text Object Model (TOM) does not support a characters collection.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>