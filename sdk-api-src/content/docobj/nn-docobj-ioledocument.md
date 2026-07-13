---
UID: NN:docobj.IOleDocument
title: IOleDocument (docobj.h)
description: Enables a document object to communicate to containers its ability to create views of its data.
helpviewer_keywords: ["IOleDocument","IOleDocument interface [COM]","IOleDocument interface [COM]","described","_ole_ioledocument","com.ioledocument","docobj/IOleDocument"]
old-location: com\ioledocument.htm
tech.root: com
ms.assetid: 7a15d6ef-900c-4a0b-8b85-60dc66ca03a3
ms.date: 12/05/2018
ms.keywords: IOleDocument, IOleDocument interface [COM], IOleDocument interface [COM],described, _ole_ioledocument, com.ioledocument, docobj/IOleDocument
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.Idl
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
 - IOleDocument
 - docobj/IOleDocument
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IOleDocument
---

# IOleDocument interface


## -description

Enables a document object to communicate to containers its ability to create views of its data. This interface also enables a document object to enumerate its views and to provide containers with miscellaneous information about itself, such as whether it supports multiple views or complex rectangles.

## -inheritance

The <b>IOleDocument</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleDocument</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-iolecommandtarget">IOleCommandTarget</a>



<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentsite">IOleDocumentSite</a>



<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>



<a href="/windows/desktop/api/docobj/nn-docobj-iprint">IPrint</a>
