---
UID: NN:docobj.IOleDocumentSite
title: IOleDocumentSite (docobj.h)
description: Enables a document that has been implemented as a document object to bypass the normal activation sequence for in-place-active objects and to directly instruct its client site to activate it as a document object.
helpviewer_keywords: ["IOleDocumentSite","IOleDocumentSite interface [COM]","IOleDocumentSite interface [COM]","described","_ole_ioledocumentsite","com.ioledocumentsite","docobj/IOleDocumentSite"]
old-location: com\ioledocumentsite.htm
tech.root: com
ms.assetid: cac435c9-caee-4751-9ad8-df48b6d4c7e0
ms.date: 12/05/2018
ms.keywords: IOleDocumentSite, IOleDocumentSite interface [COM], IOleDocumentSite interface [COM],described, _ole_ioledocumentsite, com.ioledocumentsite, docobj/IOleDocumentSite
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
 - IOleDocumentSite
 - docobj/IOleDocumentSite
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
 - IOleDocumentSite
---

# IOleDocumentSite interface


## -description

Enables a document that has been implemented as a document object to bypass the normal activation sequence for in-place-active objects and to directly instruct its client site to activate it as a document object. A client site with this ability is called a document site.

For each document object to be hosted, a container must provide a corresponding document site, which is an OLE Documents client site that, in addition to implementing <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a> and <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>, also implements <b>IOleDocumentSite</b>. Each document site implements a separate document view site object for each view of a document to be activated. The document view site implements <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a> and, optionally, <a href="/windows/desktop/api/docobj/nn-docobj-icontinuecallback">IContinueCallback</a>.

## -inheritance

The <b>IOleDocumentSite</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleDocumentSite</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrolsite">IOleControlSite</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>
