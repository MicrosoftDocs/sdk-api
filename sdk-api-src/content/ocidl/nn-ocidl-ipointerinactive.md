---
UID: NN:ocidl.IPointerInactive
title: IPointerInactive (ocidl.h)
description: Enables an object to remain inactive most of the time, yet still participate in interaction with the mouse, including drag and drop.
helpviewer_keywords: ["IPointerInactive","IPointerInactive interface [COM]","IPointerInactive interface [COM]","described","_ctrl_ipointerinactive","com.ipointerinactive","ocidl/IPointerInactive"]
old-location: com\ipointerinactive.htm
tech.root: com
ms.assetid: dc08d512-6994-419a-a460-6274ce74e40f
ms.date: 12/05/2018
ms.keywords: IPointerInactive, IPointerInactive interface [COM], IPointerInactive interface [COM],described, _ctrl_ipointerinactive, com.ipointerinactive, ocidl/IPointerInactive
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
 - IPointerInactive
 - ocidl/IPointerInactive
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
 - IPointerInactive
---

# IPointerInactive interface


## -description

Enables an object to remain inactive most of the time, yet still participate in interaction with the mouse, including drag and drop.

Objects can be active (in-place or UI active) or they can be inactive (loaded or running). An active object creates a window and can receive Windows mouse and keyboard messages. An inactive object can render itself and provide a representation of its data in a given format. While they provide more functionality, active objects also consume more resources than inactive objects. Typically, they are larger and slower than inactive objects. Thus, keeping an object inactive can provide performance improvements.

However, an object, such as a control, needs to be able to control the mouse pointer, fire mouse events, and act as a drop target so it can participate in the user interface of its container application.

## -inheritance

The <b>IPointerInactive</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPointerInactive</b> also has these types of members:

