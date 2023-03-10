---
UID: NF:tom.ITextDocument.BeginEditCollection
title: ITextDocument::BeginEditCollection (tom.h)
description: Turns on edit collection (also called undo grouping).
helpviewer_keywords: ["BeginEditCollection","BeginEditCollection method [Windows Controls]","BeginEditCollection method [Windows Controls]","ITextDocument interface","ITextDocument interface [Windows Controls]","BeginEditCollection method","ITextDocument.BeginEditCollection","ITextDocument::BeginEditCollection","_win32_ITextDocument_BeginEditCollection","_win32_ITextDocument_BeginEditCollection_cpp","controls.ITextDocument_BeginEditCollection","controls._win32_ITextDocument_BeginEditCollection","tom/ITextDocument::BeginEditCollection"]
old-location: controls\ITextDocument_BeginEditCollection.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\begineditcollection.htm
ms.date: 12/05/2018
ms.keywords: BeginEditCollection, BeginEditCollection method [Windows Controls], BeginEditCollection method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],BeginEditCollection method, ITextDocument.BeginEditCollection, ITextDocument::BeginEditCollection, _win32_ITextDocument_BeginEditCollection, _win32_ITextDocument_BeginEditCollection_cpp, controls.ITextDocument_BeginEditCollection, controls._win32_ITextDocument_BeginEditCollection, tom/ITextDocument::BeginEditCollection
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
 - ITextDocument::BeginEditCollection
 - tom/ITextDocument::BeginEditCollection
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
 - ITextDocument.BeginEditCollection
---

# ITextDocument::BeginEditCollection


## -description

Turns on edit collection (also called <i>undo grouping</i>).



## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Undo is not enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented.

</td>
</tr>
</table>

## -remarks

A single 
				<b>Undo</b> command undoes all changes made while edit collection is turned on.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument-endeditcollection">EndEditCollection</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument-freeze">Freeze</a>



<a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
