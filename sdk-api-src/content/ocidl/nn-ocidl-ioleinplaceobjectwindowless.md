---
UID: NN:ocidl.IOleInPlaceObjectWindowless
title: IOleInPlaceObjectWindowless (ocidl.h)
description: Enables a windowless object to process window messages and participate in drag and drop operations. It is derived from and extends the IOleInPlaceObject interface.
helpviewer_keywords: ["IOleInPlaceObjectWindowless","IOleInPlaceObjectWindowless interface [COM]","IOleInPlaceObjectWindowless interface [COM]","described","_ole_ioleinplaceobjectwindowless","com.ioleinplaceobjectwindowless","ocidl/IOleInPlaceObjectWindowless"]
old-location: com\ioleinplaceobjectwindowless.htm
tech.root: com
ms.assetid: 86aabb46-6bc7-4953-b4eb-8692552ca380
ms.date: 12/05/2018
ms.keywords: IOleInPlaceObjectWindowless, IOleInPlaceObjectWindowless interface [COM], IOleInPlaceObjectWindowless interface [COM],described, _ole_ioleinplaceobjectwindowless, com.ioleinplaceobjectwindowless, ocidl/IOleInPlaceObjectWindowless
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IOleInPlaceObjectWindowless
 - ocidl/IOleInPlaceObjectWindowless
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleInPlaceObjectWindowless
---

# IOleInPlaceObjectWindowless interface


## -description

Enables a windowless object to process window messages and participate in drag and drop operations. It is derived from and extends the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a> interface.

A small object, such as a control, does not need a window of its own. Instead, it can rely on its container to dispatch window messages and help the object to participate in drag and drop operations. The container must implement the <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a> interface. Otherwise, the object must act as a normal compound document object and create a window when it is activated.

## -inheritance

The <b>IOleInPlaceObjectWindowless</b> interface inherits from <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a>. <b>IOleInPlaceObjectWindowless</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceobject">IOleInPlaceObject</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>
