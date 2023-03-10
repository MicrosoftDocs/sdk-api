---
UID: NN:shobjidl_core.IPreviewHandler
title: IPreviewHandler (shobjidl_core.h)
description: Exposes methods for the display of rich previews.
helpviewer_keywords: ["IPreviewHandler","IPreviewHandler interface [Windows Shell]","IPreviewHandler interface [Windows Shell]","described","_shell_IPreviewHandler","shell.IPreviewHandler","shobjidl_core/IPreviewHandler"]
old-location: shell\IPreviewHandler.htm
tech.root: shell
ms.assetid: a4e6507c-10b1-4c21-9359-92ba635a2a2c
ms.date: 12/05/2018
ms.keywords: IPreviewHandler, IPreviewHandler interface [Windows Shell], IPreviewHandler interface [Windows Shell],described, _shell_IPreviewHandler, shell.IPreviewHandler, shobjidl_core/IPreviewHandler
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
 - IPreviewHandler
 - shobjidl_core/IPreviewHandler
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
 - IPreviewHandler
---

# IPreviewHandler interface


## -description

Exposes methods for the display of rich previews.

## -inheritance

The <b>IPreviewHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPreviewHandler</b> also has these types of members:

## -remarks

Preview handlers can be built in managed code. Typically, all preview handlers are hosted together in a surrogate process called prevhost.exe. There is one instance of this process for preview handlers running at normal integrity level, and another instance for preview handlers running at low integrity level. If you want to implement your handler in managed code, your handler should not run inside either of these shared processes. Instead, arrange for your handler to get a new instance of prevhost.exe by creating a new AppID entry in the registry (specifying prevhost.exe as the DllSurrogate value) and then setting that as the AppID value in the registry value for your handler's class ID. This will ensure that a unique prevhost.exe instance is created for your handler, instead of the common instances used by the other handlers.
