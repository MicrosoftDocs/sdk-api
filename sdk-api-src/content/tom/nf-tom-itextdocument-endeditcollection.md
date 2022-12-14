---
UID: NF:tom.ITextDocument.EndEditCollection
title: ITextDocument::EndEditCollection (tom.h)
description: Turns off edit collection (also called undo grouping).
helpviewer_keywords: ["EndEditCollection","EndEditCollection method [Windows Controls]","EndEditCollection method [Windows Controls]","ITextDocument interface","ITextDocument interface [Windows Controls]","EndEditCollection method","ITextDocument.EndEditCollection","ITextDocument::EndEditCollection","_win32_ITextDocument_EndEditCollection","_win32_ITextDocument_EndEditCollection_cpp","controls.ITextDocument_EndEditCollection","controls._win32_ITextDocument_EndEditCollection","tom/ITextDocument::EndEditCollection"]
old-location: controls\ITextDocument_EndEditCollection.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\endeditcollection.htm
ms.date: 12/05/2018
ms.keywords: EndEditCollection, EndEditCollection method [Windows Controls], EndEditCollection method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],EndEditCollection method, ITextDocument.EndEditCollection, ITextDocument::EndEditCollection, _win32_ITextDocument_EndEditCollection, _win32_ITextDocument_EndEditCollection_cpp, controls.ITextDocument_EndEditCollection, controls._win32_ITextDocument_EndEditCollection, tom/ITextDocument::EndEditCollection
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
 - ITextDocument::EndEditCollection
 - tom/ITextDocument::EndEditCollection
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
 - ITextDocument.EndEditCollection
---

# ITextDocument::EndEditCollection


## -description

Turns off edit collection (also called <i>undo grouping</i>).



## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns the following COM error code. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
This method is not implemented.

</td>
</tr>
</table>

## -remarks

The screen is unfrozen unless the freeze count is nonzero.

## -see-also

<a href="/windows/desktop/api/tom/nf-tom-itextdocument-begineditcollection">BeginEditCollection</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument-freeze">Freeze</a>



<a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
