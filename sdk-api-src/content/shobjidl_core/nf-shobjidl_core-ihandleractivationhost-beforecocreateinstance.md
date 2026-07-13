---
UID: NF:shobjidl_core.IHandlerActivationHost.BeforeCoCreateInstance
title: IHandlerActivationHost::BeforeCoCreateInstance (shobjidl_core.h)
description: . (IHandlerActivationHost.BeforeCoCreateInstance)
helpviewer_keywords: ["BeforeCoCreateInstance","BeforeCoCreateInstance method [Windows Shell]","BeforeCoCreateInstance method [Windows Shell]","IHandlerActivationHost interface","IHandlerActivationHost interface [Windows Shell]","BeforeCoCreateInstance method","IHandlerActivationHost.BeforeCoCreateInstance","IHandlerActivationHost::BeforeCoCreateInstance","shell.IHandlerActivationHost_BeforeCoCreateInstance","shobjidl_core/IHandlerActivationHost::BeforeCoCreateInstance"]
old-location: shell\IHandlerActivationHost_BeforeCoCreateInstance.htm
tech.root: shell
ms.assetid: 6ec3f90a-4b65-4cbc-a777-a338c97f1acf
ms.date: 12/05/2018
ms.keywords: BeforeCoCreateInstance, BeforeCoCreateInstance method [Windows Shell], BeforeCoCreateInstance method [Windows Shell],IHandlerActivationHost interface, IHandlerActivationHost interface [Windows Shell],BeforeCoCreateInstance method, IHandlerActivationHost.BeforeCoCreateInstance, IHandlerActivationHost::BeforeCoCreateInstance, shell.IHandlerActivationHost_BeforeCoCreateInstance, shobjidl_core/IHandlerActivationHost::BeforeCoCreateInstance
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
 - IHandlerActivationHost::BeforeCoCreateInstance
 - shobjidl_core/IHandlerActivationHost::BeforeCoCreateInstance
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
 - IHandlerActivationHost.BeforeCoCreateInstance
---

# IHandlerActivationHost::BeforeCoCreateInstance


## -description

Notifies a client of [ShellExecuteEx](../shellapi/nf-shellapi-shellexecuteexw.md) that a handler is about to be created, giving that client the opportunity to display UI confirming the use of that handler or reject it by returning a specific error code.

## -parameters

### -param clsidHandler [in]

Identifies the handler.

### -param itemsBeingActivated [in]

The Shell item objects that will be passed to the handler. Typically there is only one, but in some cases there can be more than one.

### -param handlerInfo [in]

Provides access to information about the handler that will be invoked. This object also supports **IHandlerInfo2** on versions of Windows that support that interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. 
Otherwise, it returns an <b>HRESULT</b> error code, <b>HRESULT_FROM_WIN32(ERROR_CANCELLED)</b> indicates that the ShellExecute call should be canceled, <b>EXECUTE_E_LAUNCH_APPLICATION</b> indicates that this handler should not be used, but if there is another it should be used.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost">IHandlerActivationHost</a>
