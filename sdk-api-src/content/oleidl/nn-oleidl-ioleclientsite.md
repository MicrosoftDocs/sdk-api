---
UID: NN:oleidl.IOleClientSite
title: IOleClientSite (oleidl.h)
description: Provides the primary means by which an embedded object obtains information about the location and extent of its display site, its moniker, its user interface, and other resources provided by its container.
helpviewer_keywords: ["IOleClientSite","IOleClientSite interface [COM]","IOleClientSite interface [COM]","described","_ole_ioleclientsite","com.ioleclientsite","oleidl/IOleClientSite"]
old-location: com\ioleclientsite.htm
tech.root: com
ms.assetid: dafee149-926a-4d08-a43d-5847682db645
ms.date: 12/05/2018
ms.keywords: IOleClientSite, IOleClientSite interface [COM], IOleClientSite interface [COM],described, _ole_ioleclientsite, com.ioleclientsite, oleidl/IOleClientSite
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IOleClientSite
 - oleidl/IOleClientSite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleClientSite
---

# IOleClientSite interface


## -description

Provides the primary means by which an embedded object obtains information about the location and extent of its display site, its moniker, its user interface, and other resources provided by its container. An object server calls <b>IOleClientSite</b> to request services from the container. A container must provide one instance of <b>IOleClientSite</b> for every compound-document object it contains.
<div class="alert"><b>Note</b>  This interface is not supported for use across machine boundaries.</div><div> </div>

## -inheritance

The <b>IOleClientSite</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleClientSite</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrolsite">IOleControlSite</a>



<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentsite">IOleDocumentSite</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getclientsite">IOleObject::GetClientSite</a>
