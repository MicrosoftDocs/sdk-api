---
UID: NN:tom.ITextDocument
title: ITextDocument (tom.h)
description: The ITextDocument interface is the Text Object Model (TOM) top-level interface, which retrieves the active selection and range objects for any story in the document — whether active or not.
helpviewer_keywords: ["ITextDocument","ITextDocument interface [Windows Controls]","ITextDocument interface [Windows Controls]","described","_win32_ITextDocument","_win32_ITextDocument_cpp","controls.ITextDocument","controls._win32_ITextDocument","tom/ITextDocument"]
old-location: controls\ITextDocument.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextdocument.htm
ms.date: 12/05/2018
ms.keywords: ITextDocument, ITextDocument interface [Windows Controls], ITextDocument interface [Windows Controls],described, _win32_ITextDocument, _win32_ITextDocument_cpp, controls.ITextDocument, controls._win32_ITextDocument, tom/ITextDocument
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
 - ITextDocument
 - tom/ITextDocument
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
 - ITextDocument
---

# ITextDocument interface


## -description

The <b>ITextDocument</b> interface is the Text Object Model (TOM) top-level interface, which retrieves the active selection and range objects for any story in the document—whether active or not. It enables the application to: 
        
<ul>
<li>Open and save documents.</li>
<li>Control undo behavior and screen updating.</li>
<li>Find a range from a screen position.</li>
<li>Get an <a href="/windows/desktop/api/tom/nn-tom-itextstoryranges">ITextStoryRanges</a> story enumerator.</li>
</ul><b>When to Implement</b>

Applications typically do not implement the <b>ITextDocument</b> interface. Microsoft text solutions, such as rich edit controls, implement <b>ITextDocument</b> as part of their TOM implementation. 

<b>When to Use</b>

Applications can retrieve an <b>ITextDocument</b> pointer from a rich edit control. To do this, send an <a href="/windows/desktop/Controls/em-getoleinterface">EM_GETOLEINTERFACE</a> message to retrieve an <a href="/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a> object from a rich edit control. Then, call the object's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an <b>ITextDocument</b> pointer.

## -inheritance

The <b>ITextDocument</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextDocument</b> also has these types of members:

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>



<a href="/windows/desktop/Controls/using-the-text-object-model">Using The Text Object Model</a>
