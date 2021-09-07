---
UID: NN:tom.ITextStory
title: ITextStory (tom.h)
description: The ITextStory interface methods are used to access shared data from multiple stories, which is stored in the parent ITextServices instance.
helpviewer_keywords: ["ITextStory","ITextStory interface [Windows Controls]","ITextStory interface [Windows Controls]","described","controls.itextstory","tom/ITextStory"]
old-location: controls\itextstory.htm
tech.root: Controls
ms.assetid: 8b52c6e8-c250-4cfb-979e-770df9f94010
ms.date: 12/05/2018
ms.keywords: ITextStory, ITextStory interface [Windows Controls], ITextStory interface [Windows Controls],described, controls.itextstory, tom/ITextStory
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tom.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStory
 - tom/ITextStory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tom.h
api_name:
 - ITextStory
---

# ITextStory interface


## -description

The <b>ITextStory</b> interface methods are used to access shared data from multiple stories, which is stored in the parent <a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a> instance. 

The stories can be "edited" simultaneously by using individual <a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> methods, and displayed independently of one another. In addition, one story at a time can be UI active; that is, it receives keyboard and mouse input. 


The <b>ITextStory</b> is a lightweight interface that does not require an <a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> object. This allows the client to manipulate a story, which is a faster, smaller object than a complete editing instance.

## -inheritance

The <b>ITextStory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStory</b> also has these types of members:

