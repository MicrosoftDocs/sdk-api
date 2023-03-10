---
UID: NN:shobjidl_core.IHandlerActivationHost
title: IHandlerActivationHost (shobjidl_core.h)
description: . (IHandlerActivationHost)
helpviewer_keywords: ["IHandlerActivationHost","IHandlerActivationHost interface [Windows Shell]","IHandlerActivationHost interface [Windows Shell]","described","shell.IHandlerActivationHost","shobjidl_core/IHandlerActivationHost"]
old-location: shell\IHandlerActivationHost.htm
tech.root: shell
ms.assetid: 4c60a3f8-48ec-4686-9e27-692f88cd1c55
ms.date: 12/05/2018
ms.keywords: IHandlerActivationHost, IHandlerActivationHost interface [Windows Shell], IHandlerActivationHost interface [Windows Shell],described, shell.IHandlerActivationHost, shobjidl_core/IHandlerActivationHost
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IHandlerActivationHost
 - shobjidl_core/IHandlerActivationHost
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
 - IHandlerActivationHost
---

# IHandlerActivationHost interface


## -description

Enables a client of Shell item activation (including callers of [ShellExecuteEx](../shellapi/nf-shellapi-shellexecuteexw.md) and [IContextMenu::InvokeCommand](./nf-shobjidl_core-icontextmenu-invokecommand.md)) to be given a chance to veto or perform some action before the activation of verb handlers.

## -inheritance

The <b>IHandlerActivationHost</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IHandlerActivationHost</b> also has these types of members:

## -remarks

This interface is implemented by an object reachable through the site chain provided to [ShellExecuteEx](../shellapi/nf-shellapi-shellexecuteexw.md) or the context menu handler. Applications will return this object in their **IServiceProvider::QueryService** implementation when asked for the service ID **SID_SHandlerActivationHost**.
