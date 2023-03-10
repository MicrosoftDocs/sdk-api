---
UID: NF:tom.ITextSelection.TypeText
title: ITextSelection::TypeText (tom.h)
description: Types the string given by bstr at this selection as if someone typed it. This is similar to the underlying SetText method, but is sensitive to the Insert/Overtype key state and UI settings like AutoCorrect and smart quotes.
helpviewer_keywords: ["ITextSelection interface [Windows Controls]","TypeText method","ITextSelection.TypeText","ITextSelection::TypeText","TypeText","TypeText method [Windows Controls]","TypeText method [Windows Controls]","ITextSelection interface","_win32_ITextSelection_TypeText","_win32_ITextSelection_TypeText_cpp","controls.ITextSelection_TypeText","controls._win32_ITextSelection_TypeText","tom/ITextSelection::TypeText"]
old-location: controls\ITextSelection_TypeText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\typetext.htm
ms.date: 12/05/2018
ms.keywords: ITextSelection interface [Windows Controls],TypeText method, ITextSelection.TypeText, ITextSelection::TypeText, TypeText, TypeText method [Windows Controls], TypeText method [Windows Controls],ITextSelection interface, _win32_ITextSelection_TypeText, _win32_ITextSelection_TypeText_cpp, controls.ITextSelection_TypeText, controls._win32_ITextSelection_TypeText, tom/ITextSelection::TypeText
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
 - ITextSelection::TypeText
 - tom/ITextSelection::TypeText
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
 - ITextSelection.TypeText
---

# ITextSelection::TypeText


## -description

Types the string given by <i>bstr</i> at this selection as if someone typed it. This is similar to the underlying <a href="/windows/desktop/api/tom/nf-tom-itextrange-settext">SetText</a> method, but is sensitive to the Insert/Overtype key state and UI settings like AutoCorrect and smart quotes.

## -parameters

### -param bstr

Type: <b>BSTR</b>

String to type into this selection.

## -returns

Type: <b>HRESULT</b>

The method returns an 
						<b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
bstr is null.

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

This method types the string given by <i>bstr</i> at this selection as if someone typed it. Using <b>TypeText</b> is faster than sending characters through the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> function, but it is slower than using <a href="/windows/desktop/api/tom/nf-tom-itextrange-settext">SetText</a>. 

<b>TypeText</b> is similar to the underlying <a href="/windows/desktop/api/tom/nf-tom-itextrange-settext">SetText</a> method, however, it is sensitive to the Insert/Overtype key state and UI settings like AutoCorrect and smart quotes. For example, it deletes any nondegenerate selection and then inserts or overtypes (depending on the Insert/Overtype key state—see the <a href="/windows/desktop/api/tom/nf-tom-itextselection-setflags">SetFlags</a> method) the string <i>bstr</i> at the insertion point, leaving this selection as an insertion point following the inserted text.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextselection">ITextSelection</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-setflags">SetFlags</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-settext">SetText</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>