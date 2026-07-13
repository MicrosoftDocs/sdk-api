---
UID: NN:shobjidl.INameSpaceTreeControlDropHandler
title: INameSpaceTreeControlDropHandler (shobjidl.h)
description: Exposes handler methods for drag-and-drop.
helpviewer_keywords: ["INameSpaceTreeControlDropHandler","INameSpaceTreeControlDropHandler interface [Windows Shell]","INameSpaceTreeControlDropHandler interface [Windows Shell]","described","_shell_INameSpaceTreeControlDropHandler","shell.INameSpaceTreeControlDropHandler","shobjidl/INameSpaceTreeControlDropHandler"]
old-location: shell\INameSpaceTreeControlDropHandler.htm
tech.root: shell
ms.assetid: 5d2c1783-daeb-488d-93b9-34df2712d849
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlDropHandler, INameSpaceTreeControlDropHandler interface [Windows Shell], INameSpaceTreeControlDropHandler interface [Windows Shell],described, _shell_INameSpaceTreeControlDropHandler, shell.INameSpaceTreeControlDropHandler, shobjidl/INameSpaceTreeControlDropHandler
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - INameSpaceTreeControlDropHandler
 - shobjidl/INameSpaceTreeControlDropHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeControlDropHandler
---

# INameSpaceTreeControlDropHandler interface


## -description

Exposes handler methods for drag-and-drop. Used by the namespace tree control to notify the client of any drag-and-drop operation happening within the control. Provides a way for a client to intercept a drop operation and perform its own action, or to return the desired drop effect.

## -inheritance

The <b>INameSpaceTreeControlDropHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INameSpaceTreeControlDropHandler</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a>
