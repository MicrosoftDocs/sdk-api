---
UID: NF:shobjidl_core.IShellMenuCallback.CallbackSM
title: IShellMenuCallback::CallbackSM (shobjidl_core.h)
description: Receives messages from a menu band object.
helpviewer_keywords: ["CallbackSM","CallbackSM method [Windows Shell]","CallbackSM method [Windows Shell]","IShellMenuCallback interface","IShellMenuCallback interface [Windows Shell]","CallbackSM method","IShellMenuCallback.CallbackSM","IShellMenuCallback::CallbackSM","_win32_IShellMenuCallback_CallbackSM","shell.IShellMenuCallback_CallbackSM","shobjidl_core/IShellMenuCallback::CallbackSM"]
old-location: shell\IShellMenuCallback_CallbackSM.htm
tech.root: shell
ms.assetid: 06809b61-041b-41bd-82dd-0d64edf8bbae
ms.date: 12/05/2018
ms.keywords: CallbackSM, CallbackSM method [Windows Shell], CallbackSM method [Windows Shell],IShellMenuCallback interface, IShellMenuCallback interface [Windows Shell],CallbackSM method, IShellMenuCallback.CallbackSM, IShellMenuCallback::CallbackSM, _win32_IShellMenuCallback_CallbackSM, shell.IShellMenuCallback_CallbackSM, shobjidl_core/IShellMenuCallback::CallbackSM
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellMenuCallback::CallbackSM
 - shobjidl_core/IShellMenuCallback::CallbackSM
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
 - IShellMenuCallback.CallbackSM
---

# IShellMenuCallback::CallbackSM


## -description

Receives messages from a menu band object.

## -parameters

### -param psmd [in, out]

Type: <b>LPSMDATA</b>

A pointer to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-smdata">SMDATA</a> structure that contains information about the menu.

### -param uMsg

Type: <b>UINT</b>

A message ID. This will be one of the SMC_XXX values. See <a href="/windows/desktop/shell/control-panel-applications">Shell Messages and Notifications</a> for a complete list.

### -param wParam

Type: <b>WPARAM</b>

A WPARAM value that contains additional information. See the specific SMC_XXX message reference for details.

### -param lParam

Type: <b>LPARAM</b>

An LPARAM value that contains additional information. See the specific SMC_XXX message reference for details.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.