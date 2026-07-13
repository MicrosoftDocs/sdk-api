---
UID: NF:exdisp.IShellWindows.OnActivated
title: IShellWindows::OnActivated (exdisp.h)
description: Occurs when a Shell window's activation state changes.
helpviewer_keywords: ["IShellWindows interface [Windows Shell]","OnActivated method","IShellWindows.OnActivated","IShellWindows::OnActivated","OnActivated","OnActivated method [Windows Shell]","OnActivated method [Windows Shell]","IShellWindows interface","_win32_IShellWindows_OnActivated","exdisp/IShellWindows::OnActivated","shell.IShellWindows_OnActivated"]
old-location: shell\IShellWindows_OnActivated.htm
tech.root: shell
ms.assetid: ccd93f0f-3cd2-4b18-b6d2-834665d8b658
ms.date: 12/05/2018
ms.keywords: IShellWindows interface [Windows Shell],OnActivated method, IShellWindows.OnActivated, IShellWindows::OnActivated, OnActivated, OnActivated method [Windows Shell], OnActivated method [Windows Shell],IShellWindows interface, _win32_IShellWindows_OnActivated, exdisp/IShellWindows::OnActivated, shell.IShellWindows_OnActivated
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
 - IShellWindows::OnActivated
 - exdisp/IShellWindows::OnActivated
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
 - IShellWindows.OnActivated
---

# IShellWindows::OnActivated


## -description

Occurs when a Shell window's activation state changes.

## -parameters

### -param lCookie [in]

Type: <b>long</b>

The cookie that identifies the window.

### -param fActive [in]

Type: <b>VARIANT_BOOL</b>

<b>TRUE</b> if the window is being activated; <b>FALSE</b> if the window is being deactivated.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A window is granted a cookie when it is registered as a Shell window. For more information, see <a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-register">IShellWindows::Register</a>.

## -see-also

<a href="/windows/desktop/api/exdisp/nn-exdisp-ishellwindows">IShellWindows</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-oncreated">IShellWindows::OnCreated</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-onnavigate">IShellWindows::OnNavigate</a>