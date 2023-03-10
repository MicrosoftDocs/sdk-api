---
UID: NN:oleidl.IDropTarget
title: IDropTarget (oleidl.h)
description: The IDropTarget interface is one of the interfaces you implement to provide drag-and-drop operations in your application.
helpviewer_keywords: ["IDropTarget","IDropTarget interface [COM]","IDropTarget interface [COM]","described","_ole_idroptarget","com.idroptarget","oleidl/IDropTarget"]
old-location: com\idroptarget.htm
tech.root: com
ms.assetid: 13fbe834-1ef8-4944-b2e4-9f5c413c65c8
ms.date: 12/05/2018
ms.keywords: IDropTarget, IDropTarget interface [COM], IDropTarget interface [COM],described, _ole_idroptarget, com.idroptarget, oleidl/IDropTarget
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
 - IDropTarget
 - oleidl/IDropTarget
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
 - IDropTarget
---

# IDropTarget interface


## -description

The <b>IDropTarget</b> interface is one of the interfaces you implement to provide drag-and-drop operations in your application. It contains methods used in any application that can be a target for data during a drag-and-drop operation. A drop-target application is responsible for:
<ul>
<li>Determining the effect of the drop on the target application.</li>
<li>Incorporating any valid dropped data when the drop occurs.</li>
<li>Communicating target feedback to the source so the source application can provide appropriate visual feedback such as setting the cursor.</li>
<li>Implementing drag scrolling.</li>
<li>Registering and revoking its application windows as drop targets.</li>
</ul>The <b>IDropTarget</b> interface contains methods that handle all these responsibilities except registering and revoking the application window as a drop target, for which you must call the <a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a> and the <a href="/windows/desktop/api/ole2/nf-ole2-revokedragdrop">RevokeDragDrop</a> functions.

## -inheritance

The <b>IDropTarget</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDropTarget</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsource">IDropSource</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsourcenotify">IDropSourceNotify</a>



<a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a>



<a href="/windows/desktop/api/ole2/nf-ole2-revokedragdrop">RevokeDragDrop</a>
