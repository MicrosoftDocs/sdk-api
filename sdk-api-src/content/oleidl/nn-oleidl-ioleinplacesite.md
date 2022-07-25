---
UID: NN:oleidl.IOleInPlaceSite
title: IOleInPlaceSite (oleidl.h)
description: Manages the interaction between the container and the object's in-place client site. Recall that the client site is the display site for embedded objects, and provides position and conceptual information about the object.
helpviewer_keywords: ["IOleInPlaceSite","IOleInPlaceSite interface [COM]","IOleInPlaceSite interface [COM]","described","_ole_ioleinplacesite","com.ioleinplacesite","oleidl/IOleInPlaceSite"]
old-location: com\ioleinplacesite.htm
tech.root: com
ms.assetid: 6d37e022-8c19-48b3-affb-e0eca19b5e05
ms.date: 12/05/2018
ms.keywords: IOleInPlaceSite, IOleInPlaceSite interface [COM], IOleInPlaceSite interface [COM],described, _ole_ioleinplacesite, com.ioleinplacesite, oleidl/IOleInPlaceSite
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
 - IOleInPlaceSite
 - oleidl/IOleInPlaceSite
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
 - IOleInPlaceSite
---

# IOleInPlaceSite interface


## -description

Manages the interaction between the container and the object's in-place client site. Recall that the client site is the display site for embedded objects, and provides position and conceptual information about the object.

This interface provides methods that manage in-place objects. With <b>IOleInPlaceSite</b>, you can determine if an object can be activated and manage its activation and deactivation. You can notify the container when one of its objects is being activated and inform the container that a composite menu will replace the container's regular menu. It provides methods that make it possible for the in-place object to retrieve the window object hierarchy, and the position in the parent window where the object should place its in-place activation window. Finally, it determines how the container scrolls the object, manages the object undo state, and notifies the object when its borders have changed.

## -inheritance

The <b>IOleInPlaceSite</b> interface inherits from <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IOleInPlaceSite</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>
