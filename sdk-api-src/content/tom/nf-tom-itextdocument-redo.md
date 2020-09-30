---
UID: NF:tom.ITextDocument.Redo
title: ITextDocument::Redo (tom.h)
description: Performs a specified number of redo operations.
helpviewer_keywords: ["ITextDocument interface [Windows Controls]","Redo method","ITextDocument.Redo","ITextDocument::Redo","Redo","Redo method [Windows Controls]","Redo method [Windows Controls]","ITextDocument interface","_win32_ITextDocument_Redo","_win32_ITextDocument_Redo_cpp","controls.ITextDocument_Redo","controls._win32_ITextDocument_Redo","tom/ITextDocument::Redo"]
old-location: controls\ITextDocument_Redo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\redo.htm
ms.date: 12/05/2018
ms.keywords: ITextDocument interface [Windows Controls],Redo method, ITextDocument.Redo, ITextDocument::Redo, Redo, Redo method [Windows Controls], Redo method [Windows Controls],ITextDocument interface, _win32_ITextDocument_Redo, _win32_ITextDocument_Redo_cpp, controls.ITextDocument_Redo, controls._win32_ITextDocument_Redo, tom/ITextDocument::Redo
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
 - ITextDocument::Redo
 - tom/ITextDocument::Redo
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
 - ITextDocument.Redo
---

# ITextDocument::Redo


## -description

Performs a specified number of redo operations.

## -parameters

### -param Count

Type: <b>long</b>

The number of redo operations specified.

### -param pCount

Type: <b>long*</b>

The actual count of redo operations performed. This parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If the method succeeds it returns <b>S_OK</b>. If the method fails, it returns the following COM error code. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
Less than <i>Count</i> redo operations were performed.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument-undo">Undo</a>