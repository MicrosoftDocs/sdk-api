---
UID: NN:oleidl.IOleInPlaceObject
title: IOleInPlaceObject (oleidl.h)
description: Manages the activation and deactivation of in-place objects, and determines how much of the in-place object should be visible.
helpviewer_keywords: ["IOleInPlaceObject","IOleInPlaceObject interface [COM]","IOleInPlaceObject interface [COM]","described","_ole_ioleinplaceobject","com.ioleinplaceobject","oleidl/IOleInPlaceObject"]
old-location: com\ioleinplaceobject.htm
tech.root: com
ms.assetid: c14de79d-e844-49cf-ae70-6c3e417fab90
ms.date: 12/05/2018
ms.keywords: IOleInPlaceObject, IOleInPlaceObject interface [COM], IOleInPlaceObject interface [COM],described, _ole_ioleinplaceobject, com.ioleinplaceobject, oleidl/IOleInPlaceObject
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IOleInPlaceObject
 - oleidl/IOleInPlaceObject
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
 - IOleInPlaceObject
---

# IOleInPlaceObject interface


## -description

Manages the activation and deactivation of in-place objects, and determines how much of the in-place object should be visible.

You can obtain a pointer to <b>IOleInPlaceObject</b> by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> on <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>.

## -inheritance

The <b>IOleInPlaceObject</b> interface inherits from <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IOleInPlaceObject</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>
