---
UID: NN:shobjidl.IHWEventHandler2
title: IHWEventHandler2 (shobjidl.h)
description: Extends the IHWEventHandler interface to address User Account Control (UAC) elevation for device handlers.
helpviewer_keywords: ["IHWEventHandler2","IHWEventHandler2 interface [Windows Shell]","IHWEventHandler2 interface [Windows Shell]","described","_shell_IHWEventHandler2","shell.IHWEventHandler2","shobjidl/IHWEventHandler2"]
old-location: shell\IHWEventHandler2.htm
tech.root: shell
ms.assetid: 2885bce8-3139-4158-b178-d36bb13aff0f
ms.date: 12/05/2018
ms.keywords: IHWEventHandler2, IHWEventHandler2 interface [Windows Shell], IHWEventHandler2 interface [Windows Shell],described, _shell_IHWEventHandler2, shell.IHWEventHandler2, shobjidl/IHWEventHandler2
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IHWEventHandler2
 - shobjidl/IHWEventHandler2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IHWEventHandler2
---

# IHWEventHandler2 interface


## -description

Extends the <a href="/windows/desktop/api/shobjidl/nn-shobjidl-ihweventhandler">IHWEventHandler</a> interface to address User Account Control (UAC) elevation for device handlers.

## -inheritance

The <b>IHWEventHandler2</b> interface inherits from <a href="/windows/desktop/api/shobjidl/nn-shobjidl-ihweventhandler">IHWEventHandler</a>. <b>IHWEventHandler2</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl/nn-shobjidl-ihweventhandler">IHWEventHandler</a> interface, from which it inherits.

Handlers that implement this interface should return quickly from calls to <a href="/windows/desktop/api/shobjidl/nf-shobjidl-ihweventhandler-handleevent">IHWEventHandler::HandleEvent</a> and <a href="/windows/desktop/api/shobjidl/nf-shobjidl-ihweventhandler2-handleeventwithhwnd">IHWEventHandler2::HandleEventWithHWND</a> so they do not block the AutoPlay dialog from closing. Also, if a local server must be launched for the creation of this handler, it should not block the CreateInstance call; it should return as soon as possible.
