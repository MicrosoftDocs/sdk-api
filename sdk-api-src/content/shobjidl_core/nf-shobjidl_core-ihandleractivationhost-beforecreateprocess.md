---
UID: NF:shobjidl_core.IHandlerActivationHost.BeforeCreateProcess
title: IHandlerActivationHost::BeforeCreateProcess (shobjidl_core.h)
description: . (IHandlerActivationHost.BeforeCreateProcess)
helpviewer_keywords: ["BeforeCreateProcess","BeforeCreateProcess method [Windows Shell]","BeforeCreateProcess method [Windows Shell]","IHandlerActivationHost interface","IHandlerActivationHost interface [Windows Shell]","BeforeCreateProcess method","IHandlerActivationHost.BeforeCreateProcess","IHandlerActivationHost::BeforeCreateProcess","shell.IHandlerActivationHost_BeforeCreateProcess","shobjidl_core/IHandlerActivationHost::BeforeCreateProcess"]
old-location: shell\IHandlerActivationHost_BeforeCreateProcess.htm
tech.root: shell
ms.assetid: aa0ea3cb-7fe3-498c-a105-b78492166f65
ms.date: 12/05/2018
ms.keywords: BeforeCreateProcess, BeforeCreateProcess method [Windows Shell], BeforeCreateProcess method [Windows Shell],IHandlerActivationHost interface, IHandlerActivationHost interface [Windows Shell],BeforeCreateProcess method, IHandlerActivationHost.BeforeCreateProcess, IHandlerActivationHost::BeforeCreateProcess, shell.IHandlerActivationHost_BeforeCreateProcess, shobjidl_core/IHandlerActivationHost::BeforeCreateProcess
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
 - IHandlerActivationHost::BeforeCreateProcess
 - shobjidl_core/IHandlerActivationHost::BeforeCreateProcess
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
 - IHandlerActivationHost.BeforeCreateProcess
---

# IHandlerActivationHost::BeforeCreateProcess


## -description

Notifies a client of [ShellExecuteEx](../shellapi/nf-shellapi-shellexecuteexw.md) that a process is about to created, giving that client the opportunity to display UI confirming that or reject it by returning a specific error code.

## -parameters

### -param applicationPath [in]

The fully qualified path to the process executable, or in some cases a DLL path.

### -param commandLine [in]

The full command line that will be passed to **CreateProcess** including the arguments that the handler requested via its registration.

### -param handlerInfo [in]

Provides access to information about the handler that will be invoked. This object also supports **IHandlerInfo2** on versions of windows that support that interface. This object also implements [IObjectWithSelection](./nn-shobjidl_core-iobjectwithselection.md). This can be used to get the Shell item, or items in some cases, that are being launched.

## -returns

If this method succeeds, it returns <b>S_OK</b>. 
Otherwise, it returns an <b>HRESULT</b> error code, <b>HRESULT_FROM_WIN32(ERROR_CANCELLED)</b> indicates that the ShellExecute call should be canceled.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost">IHandlerActivationHost</a>
