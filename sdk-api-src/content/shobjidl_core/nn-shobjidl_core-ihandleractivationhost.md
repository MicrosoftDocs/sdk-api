---
UID: NN:shobjidl_core.IHandlerActivationHost
title: IHandlerActivationHost (shobjidl_core.h)
description: .helpviewer_keywords: ["IHandlerActivationHost","IHandlerActivationHost interface [Windows Shell]","IHandlerActivationHost interface [Windows Shell]","described","shell.IHandlerActivationHost","shobjidl_core/IHandlerActivationHost"]
old-location: shell\IHandlerActivationHost.htm
tech.root: shell
ms.assetid: 4c60a3f8-48ec-4686-9e27-692f88cd1c55
ms.date: 12/05/2018
ms.keywords: IHandlerActivationHost, IHandlerActivationHost interface [Windows Shell], IHandlerActivationHost interface [Windows Shell],described, shell.IHandlerActivationHost, shobjidl_core/IHandlerActivationHost
f1_keywords:
- shobjidl_core/IHandlerActivationHost
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IHandlerActivationHost
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IHandlerActivationHost interface


## -description

Enables a client of Shell item activation (including callers of [ShellExecuteEx](/windows/win32/api/shellapi/nf-shellapi-shellexecuteexw) and [IContextMenu::InvokeCommand](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)) to be given a chance to veto or perform some action before the activation of verb handlers.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHandlerActivationHost</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IHandlerActivationHost</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IHandlerActivationHost</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ihandleractivationhost-beforecocreateinstance">BeforeCoCreateInstance</a>
</td>
<td align="left" width="63%">Notifies a client of <a href="/windows/win32/api/shellapi/nf-shellapi-shellexecuteexw">ShellExecuteEx</a> that a handler is about to be created, giving that client the opportunity to display UI confirming the use of that handler or reject it by returning a specific error code.</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ihandleractivationhost-beforecreateprocess">BeforeCreateProcess</a>
</td>
<td align="left" width="63%">Notifies a client of <a href="/windows/win32/api/shellapi/nf-shellapi-shellexecuteexw">ShellExecuteEx</a> that a process is about to created, giving that client the opportunity to display UI confirming that or reject it by returning a specific error code.</td>
</tr>
</table> 

## -remarks

This interface is implemented by an object reachable through the site chain provided to [ShellExecuteEx](/windows/win32/api/shellapi/nf-shellapi-shellexecuteexw) or the context menu handler. Applications will return this object in their **IServiceProvider::QueryService** implementation when asked for the service ID **SID_SHandlerActivationHost**.

