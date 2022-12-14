---
UID: NN:shobjidl_core.IPreviewHandlerFrame
title: IPreviewHandlerFrame (shobjidl_core.h)
description: Enables preview handlers to pass keyboard shortcuts to the host. This interface retrieves a list of keyboard shortcuts and directs the host to handle a keyboard shortcut.
helpviewer_keywords: ["IPreviewHandlerFrame","IPreviewHandlerFrame interface [Windows Shell]","IPreviewHandlerFrame interface [Windows Shell]","described","_shell_IPreviewHandlerFrame","shell.IPreviewHandlerFrame","shobjidl_core/IPreviewHandlerFrame"]
old-location: shell\IPreviewHandlerFrame.htm
tech.root: shell
ms.assetid: 4e1316e5-f736-4a9b-887b-ddc48a615c42
ms.date: 12/05/2018
ms.keywords: IPreviewHandlerFrame, IPreviewHandlerFrame interface [Windows Shell], IPreviewHandlerFrame interface [Windows Shell],described, _shell_IPreviewHandlerFrame, shell.IPreviewHandlerFrame, shobjidl_core/IPreviewHandlerFrame
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Search 4 or later
ms.custom: 19H1
f1_keywords:
 - IPreviewHandlerFrame
 - shobjidl_core/IPreviewHandlerFrame
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IPreviewHandlerFrame
---

# IPreviewHandlerFrame interface


## -description

Enables preview handlers to pass keyboard shortcuts to the host. This interface retrieves a list of keyboard shortcuts and directs the host to handle a keyboard shortcut.

## -inheritance

The <b>IPreviewHandlerFrame</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPreviewHandlerFrame</b> also has these types of members:

## -remarks

This is an interface that preview handlers use to communicate keyboard shortcuts to the host. Preview handlers obtain this interface by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the pointer passed as a parameter to <a href="/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite">SetSite</a>. Preview handlers do not need to implement this interface.
