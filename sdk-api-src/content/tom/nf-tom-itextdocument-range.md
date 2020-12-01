---
UID: NF:tom.ITextDocument.Range
title: ITextDocument::Range (tom.h)
description: Retrieves a text range object for a specified range of content in the active story of the document.
helpviewer_keywords: ["ITextDocument interface [Windows Controls]","Range method","ITextDocument.Range","ITextDocument::Range","Range","Range method [Windows Controls]","Range method [Windows Controls]","ITextDocument interface","_win32_ITextDocument_Range","_win32_ITextDocument_Range_cpp","controls.ITextDocument_Range","controls._win32_ITextDocument_Range","tom/ITextDocument::Range"]
old-location: controls\ITextDocument_Range.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\range.htm
ms.date: 12/05/2018
ms.keywords: ITextDocument interface [Windows Controls],Range method, ITextDocument.Range, ITextDocument::Range, Range, Range method [Windows Controls], Range method [Windows Controls],ITextDocument interface, _win32_ITextDocument_Range, _win32_ITextDocument_Range_cpp, controls.ITextDocument_Range, controls._win32_ITextDocument_Range, tom/ITextDocument::Range
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
 - ITextDocument::Range
 - tom/ITextDocument::Range
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
 - ITextDocument.Range
---

# ITextDocument::Range


## -description

Retrieves a text range object for a specified range of content in the active story of the document.

## -parameters

### -param cpActive

Type: <b>long</b>

The start position of new range. The default value is zero, which represents the start of the document.

### -param cpAnchor

Type: <b>long</b>

The end position of new range. The default value is zero.

### -param ppRange

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>**</b>

Address of a pointer to a variable of type <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> that receives a pointer to the specified text range.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>