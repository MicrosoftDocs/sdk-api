---
UID: NN:oleidl.IViewObject
title: IViewObject (oleidl.h)
description: Enables an object to display itself directly without passing a data object to the caller. In addition, this interface can create and manage a connection with an advise sink so the caller can be notified of changes in the view object.
helpviewer_keywords: ["IViewObject","IViewObject interface [COM]","IViewObject interface [COM]","described","_ole_iviewobject","com.iviewobject","oleidl/IViewObject"]
old-location: com\iviewobject.htm
tech.root: com
ms.assetid: 4310c987-3542-4a59-a6fb-951143001741
ms.date: 12/05/2018
ms.keywords: IViewObject, IViewObject interface [COM], IViewObject interface [COM],described, _ole_iviewobject, com.iviewobject, oleidl/IViewObject
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
 - IViewObject
 - oleidl/IViewObject
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
 - IViewObject
---

# IViewObject interface


## -description

Enables an object to display itself directly without passing a data object to the caller. In addition, this interface can create and manage a connection with an advise sink so the caller can be notified of changes in the view object.

The caller can request specific representations and specific target devices. For example, a caller can ask for either an object's content or an iconic representation. Also, the caller can ask the object to compose a picture for a target device that is independent of the drawing device context. As a result, the picture can be composed for one target device and drawn on another device context. For example, to provide a print preview operation, you can compose the drawing for a printer target device but actually draw the representation on the display.

The <b>IViewObject</b> interface is similar to <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>; except that <b>IViewObject</b> places a representation of the data onto a device context while <b>IDataObject</b> places the representation onto a transfer medium.

Unlike most other interfaces, <b>IViewObject</b> cannot be marshaled to another process. This is because device contexts are only effective in the context of one process.

## -inheritance

The <b>IViewObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IViewObject</b> also has these types of members:

