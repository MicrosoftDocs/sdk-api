---
UID: NN:shobjidl.IHWEventHandler
title: IHWEventHandler (shobjidl.h)
description: Called by AutoPlay to implement the handling of registered media types.
helpviewer_keywords: ["IHWEventHandler","IHWEventHandler interface [Windows Shell]","IHWEventHandler interface [Windows Shell]","described","inet_IHWEventHandler","shell.IHWEventHandler","shobjidl/IHWEventHandler"]
old-location: shell\IHWEventHandler.htm
tech.root: shell
ms.assetid: be49322a-99b2-4626-8e9d-29965bbe182d
ms.date: 12/05/2018
ms.keywords: IHWEventHandler, IHWEventHandler interface [Windows Shell], IHWEventHandler interface [Windows Shell],described, inet_IHWEventHandler, shell.IHWEventHandler, shobjidl/IHWEventHandler
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.5 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IHWEventHandler
 - shobjidl/IHWEventHandler
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
 - IHWEventHandler
---

# IHWEventHandler interface


## -description

Called by AutoPlay to implement the handling of registered media types.

## -inheritance

The <b>IHWEventHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IHWEventHandler</b> also has these types of members:

## -remarks

Developers supporting this interface must expose it in a Component Object Model (COM) server.

All applications registered as AutoPlay media handlers must implement this interface. Handlers that implement this interface should return quickly from calls to <a href="/windows/desktop/api/shobjidl/nf-shobjidl-ihweventhandler-handleevent">IHWEventHandler::HandleEvent</a> and  <a href="/windows/desktop/api/shobjidl/nf-shobjidl-ihweventhandler2-handleeventwithhwnd">IHWEventHandler2::HandleEventWithHWND</a> so they won't block the AutoPlay dialog from closing. Additionally, if a local server must be launched for the creation of this handler, it should not block the CreateInstance call; it should return as soon as possible.
