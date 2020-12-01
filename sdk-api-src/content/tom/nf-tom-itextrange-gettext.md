---
UID: NF:tom.ITextRange.GetText
title: ITextRange::GetText (tom.h)
description: Gets the plain text in this range. The Text property is the default property of the ITextRange interface.
helpviewer_keywords: ["GetText","GetText method [Windows Controls]","GetText method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","GetText method","ITextRange.GetText","ITextRange::GetText","_win32_ITextRange_GetText","_win32_ITextRange_GetText_cpp","controls.ITextRange_GetText","controls._win32_ITextRange_GetText","tom/ITextRange::GetText"]
old-location: controls\ITextRange_GetText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\gettext.htm
ms.date: 12/05/2018
ms.keywords: GetText, GetText method [Windows Controls], GetText method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetText method, ITextRange.GetText, ITextRange::GetText, _win32_ITextRange_GetText, _win32_ITextRange_GetText_cpp, controls.ITextRange_GetText, controls._win32_ITextRange_GetText, tom/ITextRange::GetText
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
 - ITextRange::GetText
 - tom/ITextRange::GetText
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
 - ITextRange.GetText
---

# ITextRange::GetText


## -description

Gets the plain text in this range. The Text property is the default property of the <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> interface.

## -parameters

### -param pbstr

Type: <b>BSTR*</b>

The text.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
<i>pbstr</i> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to hold the text.

</td>
</tr>
</table>

## -remarks

The <b>ITextRange::GetText</b> method returns the plain text in the range. The Text property is the default property for <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>; this is, it is automatically invoked for a range, as  in the following Microsoft Visual Basic for Applications (VBA) example.

<code>print range</code>

Some of the examples below use this fact. The <a href="/windows/desktop/api/tom/nf-tom-itextrange-settext">ITextRange::SetText</a> method substitutes <i>bstr</i> for the range text. For processing a single character, the Char property is more efficient than the Text property and does not require creating a single character range for storing a character. If the range is degenerate, the Text property lets you insert text easily. You can also delete the text in a range, as shown in the following VBA examples.
            

<code>range.delete</code>

<code>range = ""</code>

You can use the <b>Text</b> property to copy plain text from one place to another, simply by setting one range equal to another. (This is quite different from the <b>Duplicate</b> property; for more information, see <a href="/windows/desktop/api/tom/nf-tom-itextrange-getduplicate">ITextRange::GetDuplicate</a>). The following Microsoft Visual Basic example statement
                sets the text in the range1 to that in range2.

<code>range1 = range2            ' Replace range1's text by range2's</code>

The ranges can be in different stories or even in different applications. However, they do imply copying the text first into a <b>BSTR</b> and then from that string to the target location. For large amounts of text, the <a href="/windows/desktop/api/tom/nf-tom-itextrange-copy">ITextRange::Copy</a> and <a href="/windows/desktop/api/tom/nf-tom-itextrange-paste">ITextRange::Paste</a> methods can be faster, since they can perform the copy directly from source to target and with any format supported by the source and target.

The text returned by the Text property is given in Unicode. The end-of-paragraph mark may be given by 0x2029 (the Unicode Paragraph Separator), or by carriage return/line feed (CR/LF) (0xd, 0xa), or by a carriage return alone, depending on the original file. Microsoft Word uses a carriage return alone, unless it reads another choice in from a file, the clipboard, or an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>. The placeholder for an embedded object is given by the special character, <b>WCH_EMBEDDING</b>, which has the Unicode value 0xFFFC.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-copy">Copy</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-getduplicate">GetDuplicate</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-paste">Paste</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>