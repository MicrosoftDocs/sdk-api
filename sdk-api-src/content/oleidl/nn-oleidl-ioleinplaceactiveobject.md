---
UID: NN:oleidl.IOleInPlaceActiveObject
title: IOleInPlaceActiveObject (oleidl.h)
description: Provides a direct channel of communication between an in-place object and the associated application's outer-most frame window and the document window within the application that contains the embedded object.
helpviewer_keywords: ["IOleInPlaceActiveObject","IOleInPlaceActiveObject interface [COM]","IOleInPlaceActiveObject interface [COM]","described","_ole_ioleinplaceactiveobject","com.ioleinplaceactiveobject","oleidl/IOleInPlaceActiveObject"]
old-location: com\ioleinplaceactiveobject.htm
tech.root: com
ms.assetid: b077c256-1109-494c-95c2-2d33bccbe47b
ms.date: 12/05/2018
ms.keywords: IOleInPlaceActiveObject, IOleInPlaceActiveObject interface [COM], IOleInPlaceActiveObject interface [COM],described, _ole_ioleinplaceactiveobject, com.ioleinplaceactiveobject, oleidl/IOleInPlaceActiveObject
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
 - IOleInPlaceActiveObject
 - oleidl/IOleInPlaceActiveObject
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
 - IOleInPlaceActiveObject
---

# IOleInPlaceActiveObject interface


## -description

Provides a direct channel of communication between an in-place object and the associated application's outer-most frame window and the document window within the application that contains the embedded object. The communication involves the translation of messages, the state of the frame window (activated or deactivated), and the state of the document window (activated or deactivated). Also, it informs the object when it needs to resize its borders, and manages modeless dialog boxes.

## -inheritance

The <b>IOleInPlaceActiveObject</b> interface inherits from <b>IOleWindow</b>. <b>IOleInPlaceActiveObject</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>
