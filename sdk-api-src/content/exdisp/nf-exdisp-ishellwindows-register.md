---
UID: NF:exdisp.IShellWindows.Register
title: IShellWindows::Register (exdisp.h)
description: Registers an open window as a Shell window; the window is specified by handle.
helpviewer_keywords: ["IShellWindows interface [Windows Shell]","Register method","IShellWindows.Register","IShellWindows::Register","Register","Register method [Windows Shell]","Register method [Windows Shell]","IShellWindows interface","_win32_IShellWindows_Register","exdisp/IShellWindows::Register","shell.IShellWindows_Register"]
old-location: shell\IShellWindows_Register.htm
tech.root: shell
ms.assetid: 4545cc34-2209-41a5-ab65-283f2985cce0
ms.date: 12/05/2018
ms.keywords: IShellWindows interface [Windows Shell],Register method, IShellWindows.Register, IShellWindows::Register, Register, Register method [Windows Shell], Register method [Windows Shell],IShellWindows interface, _win32_IShellWindows_Register, exdisp/IShellWindows::Register, shell.IShellWindows_Register
req.header: exdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Exdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shdocvw.dll (version 5.00.2014.0216 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5
ms.custom: 19H1
f1_keywords:
 - IShellWindows::Register
 - exdisp/IShellWindows::Register
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IShellWindows.Register
---

# IShellWindows::Register


## -description

Registers an open window as a Shell window; the window is specified by handle.

## -parameters

### -param pid [in]

Type: <b><a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>*</b>

The window's <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface.

### -param hwnd [in]

Type: <b>long</b>

A handle that specifies the window to register.

### -param swClass [in]

Type: <b>int</b>

A member of <a href="/windows/desktop/api/exdisp/ne-exdisp-shellwindowtypeconstants">ShellWindowTypeConstants</a> that specifies the type of window.

### -param plCookie [out]

Type: <b>long*</b>

The window's cookie.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In the context of the Shell windows collection, a <i>cookie</i> is a token that uniquely identifies a registered Shell window.

Use this method to register an open window; if the window is pending open, use <a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-registerpending">IShellWindows::RegisterPending</a> instead.

## -see-also

<a href="/windows/desktop/api/exdisp/nn-exdisp-ishellwindows">IShellWindows</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-registerpending">IShellWindows::RegisterPending</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-revoke">IShellWindows::Revoke</a>