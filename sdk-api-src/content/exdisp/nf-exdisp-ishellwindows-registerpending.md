---
UID: NF:exdisp.IShellWindows.RegisterPending
title: IShellWindows::RegisterPending (exdisp.h)
description: Registers a pending window as a Shell window; the window is specified by an absolute PIDL.
helpviewer_keywords: ["IShellWindows interface [Windows Shell]","RegisterPending method","IShellWindows.RegisterPending","IShellWindows::RegisterPending","RegisterPending","RegisterPending method [Windows Shell]","RegisterPending method [Windows Shell]","IShellWindows interface","_win32_IShellWindows_RegisterPending","exdisp/IShellWindows::RegisterPending","shell.IShellWindows_RegisterPending"]
old-location: shell\IShellWindows_RegisterPending.htm
tech.root: shell
ms.assetid: 75e8b82c-a94e-4aad-a224-f12b22b8a4b2
ms.date: 12/05/2018
ms.keywords: IShellWindows interface [Windows Shell],RegisterPending method, IShellWindows.RegisterPending, IShellWindows::RegisterPending, RegisterPending, RegisterPending method [Windows Shell], RegisterPending method [Windows Shell],IShellWindows interface, _win32_IShellWindows_RegisterPending, exdisp/IShellWindows::RegisterPending, shell.IShellWindows_RegisterPending
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
 - IShellWindows::RegisterPending
 - exdisp/IShellWindows::RegisterPending
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
 - IShellWindows.RegisterPending
---

# IShellWindows::RegisterPending


## -description

Registers a pending window as a Shell window; the window is specified by an absolute PIDL.

## -parameters

### -param lThreadId

A thread ID.

### -param pvarloc [in]

Type: <b>VARIANT*</b>

A <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> of type VT_VARIANT | VT_BYREF. Set the value of <i>pvarloc</i> to an absolute <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">PIDL</a> (PIDLIST_ABSOLUTE) that specifies the window to register.

### -param pvarlocRoot [in]

Type: <b>VARIANT*</b>

Must be <b>NULL</b> or of type VT_EMPTY.

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

Use this method to register a window that is pending open; if the window is already open, use <a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-register">IShellWindows::Register</a> instead. Use <a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-revoke">IShellWindows::Revoke</a> to un-register a window.

## -see-also

<a href="/windows/desktop/api/exdisp/nn-exdisp-ishellwindows">IShellWindows</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-register">IShellWindows::Register</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-revoke">IShellWindows::Revoke</a>