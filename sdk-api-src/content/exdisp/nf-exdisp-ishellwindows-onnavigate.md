---
UID: NF:exdisp.IShellWindows.OnNavigate
title: IShellWindows::OnNavigate (exdisp.h)
description: Occurs when a Shell window is navigated to a new location.
helpviewer_keywords: ["IShellWindows interface [Windows Shell]","OnNavigate method","IShellWindows.OnNavigate","IShellWindows::OnNavigate","OnNavigate","OnNavigate method [Windows Shell]","OnNavigate method [Windows Shell]","IShellWindows interface","_win32_IShellWindows_OnNavigate","exdisp/IShellWindows::OnNavigate","shell.IShellWindows_OnNavigate"]
old-location: shell\IShellWindows_OnNavigate.htm
tech.root: shell
ms.assetid: b65bc979-db32-48b3-b71f-fd389957b265
ms.date: 12/05/2018
ms.keywords: IShellWindows interface [Windows Shell],OnNavigate method, IShellWindows.OnNavigate, IShellWindows::OnNavigate, OnNavigate, OnNavigate method [Windows Shell], OnNavigate method [Windows Shell],IShellWindows interface, _win32_IShellWindows_OnNavigate, exdisp/IShellWindows::OnNavigate, shell.IShellWindows_OnNavigate
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
 - IShellWindows::OnNavigate
 - exdisp/IShellWindows::OnNavigate
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
 - IShellWindows.OnNavigate
---

# IShellWindows::OnNavigate


## -description

Occurs when a Shell window is navigated to a new location.

## -parameters

### -param lCookie [in]

Type: <b>long</b>

The cookie that identifies the window.

### -param pvarLoc [in]

Type: <b>VARIANT*</b>

A <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> of type VT_VARIANT | VT_BYREF. Set the value of <i>pvarLoc</i> to an absolute <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">PIDL</a> (PIDLIST_ABSOLUTE) that specifies the new location.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A window is granted a cookie when it is registered as a Shell window. For more information, see <a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-register">IShellWindows::Register</a>.

## -see-also

<a href="/windows/desktop/api/exdisp/nn-exdisp-ishellwindows">IShellWindows</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-onactivated">IShellWindows::OnActivated</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-oncreated">IShellWindows::OnCreated</a>