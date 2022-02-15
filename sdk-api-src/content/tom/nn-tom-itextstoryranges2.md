---
UID: NN:tom.ITextStoryRanges2
title: ITextStoryRanges2 (tom.h)
description: The ITextStoryRanges2 interface enumerates the stories in an ITextDocument.
helpviewer_keywords: ["ITextStoryRanges2","ITextStoryRanges2 interface [Windows Controls]","ITextStoryRanges2 interface [Windows Controls]","described","controls.itextstoryranges2","tom/ITextStoryRanges2"]
old-location: controls\itextstoryranges2.htm
tech.root: Controls
ms.assetid: 24e2dd79-8054-44e3-aa68-778a96e2f66a
ms.date: 12/05/2018
ms.keywords: ITextStoryRanges2, ITextStoryRanges2 interface [Windows Controls], ITextStoryRanges2 interface [Windows Controls],described, controls.itextstoryranges2, tom/ITextStoryRanges2
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ITextStoryRanges2
 - tom/ITextStoryRanges2
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
 - ITextStoryRanges2
---

# ITextStoryRanges2 interface


## -description

The <b>ITextStoryRanges2</b> interface enumerates the stories in an <a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>.

You get a pointer to an <b>ITextStoryRanges2</b> collection by using the <a href="/windows/desktop/api/tom/nf-tom-itextdocument-getstoryranges">ITextDocument::GetStoryRanges</a> method. Each story obtained from this collection is represented by an <a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> object that covers the whole story. 

A Text Object Model (TOM) implementation that has only a single story doesn't need to implement the <b>ITextStoryRanges2</b> interface. An implementation of this interface should only retrieve a stories collection if <a href="/windows/desktop/api/tom/nf-tom-itextdocument-getstorycount">ITextDocument::GetStoryCount</a> returns a story count greater than one.

## -inheritance

The <b>ITextStoryRanges2</b> interface inherits from <b>ITextStoryRanges</b>. <b>ITextStoryRanges2</b> also has these types of members:

