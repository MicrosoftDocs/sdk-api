---
UID: NF:exdisp.IShellWindows.OnCreated
title: IShellWindows::OnCreated (exdisp.h)
description: Occurs when a new Shell window is created for a frame.
helpviewer_keywords: ["IShellWindows interface [Windows Shell]","OnCreated method","IShellWindows.OnCreated","IShellWindows::OnCreated","OnCreated","OnCreated method [Windows Shell]","OnCreated method [Windows Shell]","IShellWindows interface","_win32_IShellWindows_OnCreated","exdisp/IShellWindows::OnCreated","shell.IShellWindows_OnCreated"]
old-location: shell\IShellWindows_OnCreated.htm
tech.root: shell
ms.assetid: ef2f75fe-dc93-403d-af1a-c08c45e2d818
ms.date: 12/05/2018
ms.keywords: IShellWindows interface [Windows Shell],OnCreated method, IShellWindows.OnCreated, IShellWindows::OnCreated, OnCreated, OnCreated method [Windows Shell], OnCreated method [Windows Shell],IShellWindows interface, _win32_IShellWindows_OnCreated, exdisp/IShellWindows::OnCreated, shell.IShellWindows_OnCreated
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
 - IShellWindows::OnCreated
 - exdisp/IShellWindows::OnCreated
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
 - IShellWindows.OnCreated
---

# IShellWindows::OnCreated


## -description

Occurs when a new Shell window is created for a frame.

## -parameters

### -param lCookie [in]

Type: <b>long</b>

The cookie that identifies the window.

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

The address of the new window's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A window is granted a cookie when it is registered as a Shell window. For more information, see <a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-register">IShellWindows::Register</a>.

## -see-also

<a href="/windows/desktop/api/exdisp/nn-exdisp-ishellwindows">IShellWindows</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-onactivated">IShellWindows::OnActivated</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-onnavigate">IShellWindows::OnNavigate</a>