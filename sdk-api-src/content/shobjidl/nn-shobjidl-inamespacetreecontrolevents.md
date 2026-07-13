---
UID: NN:shobjidl.INameSpaceTreeControlEvents
title: INameSpaceTreeControlEvents (shobjidl.h)
description: Exposes methods for handling INameSpaceTreeControl events.
helpviewer_keywords: ["INameSpaceTreeControlEvents","INameSpaceTreeControlEvents interface [Windows Shell]","INameSpaceTreeControlEvents interface [Windows Shell]","described","_shell_INameSpaceTreeControlEvents","shell.INameSpaceTreeControlEvents","shobjidl/INameSpaceTreeControlEvents"]
old-location: shell\INameSpaceTreeControlEvents.htm
tech.root: shell
ms.assetid: 496fa657-c27c-4f6c-a137-fb0d393aa284
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents, INameSpaceTreeControlEvents interface [Windows Shell], INameSpaceTreeControlEvents interface [Windows Shell],described, _shell_INameSpaceTreeControlEvents, shell.INameSpaceTreeControlEvents, shobjidl/INameSpaceTreeControlEvents
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
 - INameSpaceTreeControlEvents
 - shobjidl/INameSpaceTreeControlEvents
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
 - INameSpaceTreeControlEvents
---

# INameSpaceTreeControlEvents interface


## -description

Exposes methods for handling <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a> events.

## -inheritance

The <b>INameSpaceTreeControlEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INameSpaceTreeControlEvents</b> also has these types of members:

## -remarks

This interface is implemented by a client of namespace control (CLSID_NameSpaceTreeControl) to be advised of namespace control events so that the client may process these events and if not, allow the namespace control to process them.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a>
