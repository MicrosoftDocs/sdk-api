---
UID: NF:tom.ITextDocument.New
title: ITextDocument::New (tom.h)
description: Opens a new document.
helpviewer_keywords: ["ITextDocument interface [Windows Controls]","New method","ITextDocument.New","ITextDocument::New","New","New method [Windows Controls]","New method [Windows Controls]","ITextDocument interface","_win32_ITextDocument_New","_win32_ITextDocument_New_cpp","controls.ITextDocument_New","controls._win32_ITextDocument_New","tom/ITextDocument::New"]
old-location: controls\ITextDocument_New.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\new.htm
ms.date: 12/05/2018
ms.keywords: ITextDocument interface [Windows Controls],New method, ITextDocument.New, ITextDocument::New, New, New method [Windows Controls], New method [Windows Controls],ITextDocument interface, _win32_ITextDocument_New, _win32_ITextDocument_New_cpp, controls.ITextDocument_New, controls._win32_ITextDocument_New, tom/ITextDocument::New
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
 - ITextDocument::New
 - tom/ITextDocument::New
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
 - ITextDocument.New
---

# ITextDocument::New


## -description

Opens a new document.



## -returns

Type: <b>HRESULT</b>

If the <b>ITextDocument::New</b> method succeeds, it returns <b>S_OK</b>.

## -remarks

If another document is open, this method saves any current changes and closes the current document before opening a new one.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument-open">Open</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
