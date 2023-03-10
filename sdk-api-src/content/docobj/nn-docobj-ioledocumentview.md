---
UID: NN:docobj.IOleDocumentView
title: IOleDocumentView (docobj.h)
description: The IOleDocumentView interface enables a container to communicate with each view supported by a document object.
helpviewer_keywords: ["IOleDocumentView","IOleDocumentView interface [COM]","IOleDocumentView interface [COM]","described","_ole_ioledocumentview","com.ioledocumentview","docobj/IOleDocumentView"]
old-location: com\ioledocumentview.htm
tech.root: com
ms.assetid: 07948c08-f047-4ae0-a41b-5410b4bbf4d6
ms.date: 12/05/2018
ms.keywords: IOleDocumentView, IOleDocumentView interface [COM], IOleDocumentView interface [COM],described, _ole_ioledocumentview, com.ioledocumentview, docobj/IOleDocumentView
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
 - IOleDocumentView
 - docobj/IOleDocumentView
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
 - IOleDocumentView
---

# IOleDocumentView interface


## -description

The <b>IOleDocumentView</b> interface enables a container to communicate with each view supported by a document object.

A document object that supports multiple views of its data represents each view as a separate object. Each document view object implements <b>IOleDocumentView</b>, along with <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a>, <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceactiveobject">IOleInPlaceActiveObject</a>, and optional interfaces such as <a href="/windows/desktop/api/docobj/nn-docobj-iprint">IPrint</a> and <a href="/windows/desktop/api/docobj/nn-docobj-iolecommandtarget">IOleCommandTarget</a>. A document object that supports only a single view does not require that view to be implemented as a separate object. Instead, both document and view can be implemented as a single class.

## -inheritance

The <b>IOleDocumentView</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleDocumentView</b> also has these types of members:

