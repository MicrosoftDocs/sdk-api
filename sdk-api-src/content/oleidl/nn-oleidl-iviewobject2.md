---
UID: NN:oleidl.IViewObject2
title: IViewObject2 (oleidl.h)
description: An extension to the IViewObject interface which returns the size of the drawing for a given view of an object. You can prevent the object from being run if it isn't already running by calling this method instead of IOleObject::GetExtent.
helpviewer_keywords: ["IViewObject2","IViewObject2 interface [COM]","IViewObject2 interface [COM]","described","_ole_iviewobject2","com.iviewobject2","oleidl/IViewObject2"]
old-location: com\iviewobject2.htm
tech.root: com
ms.assetid: b150ca4b-c53c-4bcb-85fa-461f9fa8b63b
ms.date: 12/05/2018
ms.keywords: IViewObject2, IViewObject2 interface [COM], IViewObject2 interface [COM],described, _ole_iviewobject2, com.iviewobject2, oleidl/IViewObject2
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
 - IViewObject2
 - oleidl/IViewObject2
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
 - IViewObject2
---

# IViewObject2 interface


## -description

An extension to the <a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a> interface which returns the size of the drawing for a given view of an object. You can prevent the object from being run if it isn't already running by calling this method instead of <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getextent">IOleObject::GetExtent</a>.

Like the <a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a> interface, <b>IViewObject2</b> cannot be marshaled to another process. This is because device contexts are only effective in the context of one process.

The OLE-provided default implementation provides the size of the object in the cache.

## -inheritance

The <b>IViewObject2</b> interface inherits from <a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a>. <b>IViewObject2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a>
