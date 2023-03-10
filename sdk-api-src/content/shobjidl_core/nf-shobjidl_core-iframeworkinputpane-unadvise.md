---
UID: NF:shobjidl_core.IFrameworkInputPane.Unadvise
title: IFrameworkInputPane::Unadvise (shobjidl_core.h)
description: Unregisters an app's input pane handler object so that it no longer receives notifications.
helpviewer_keywords: ["IFrameworkInputPane interface [Windows Shell]","Unadvise method","IFrameworkInputPane.Unadvise","IFrameworkInputPane::Unadvise","Unadvise","Unadvise method [Windows Shell]","Unadvise method [Windows Shell]","IFrameworkInputPane interface","shell.IFrameworkInputPane_Unadvise","shobjidl_core/IFrameworkInputPane::Unadvise"]
old-location: shell\IFrameworkInputPane_Unadvise.htm
tech.root: shell
ms.assetid: E4187EC2-DD8F-4e3c-BD0C-B5AD4B02E943
ms.date: 12/05/2018
ms.keywords: IFrameworkInputPane interface [Windows Shell],Unadvise method, IFrameworkInputPane.Unadvise, IFrameworkInputPane::Unadvise, Unadvise, Unadvise method [Windows Shell], Unadvise method [Windows Shell],IFrameworkInputPane interface, shell.IFrameworkInputPane_Unadvise, shobjidl_core/IFrameworkInputPane::Unadvise
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
 - IFrameworkInputPane::Unadvise
 - shobjidl_core/IFrameworkInputPane::Unadvise
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
 - IFrameworkInputPane.Unadvise
---

# IFrameworkInputPane::Unadvise


## -description

Unregisters an app's input pane handler object so that it no longer receives notifications.

## -parameters

### -param dwCookie [in]

Type: <b>DWORD</b>

A cookie that identifies the handler. This value was obtained when you registered the handler through the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-advise">Advise</a> method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpane">IFrameworkInputPane</a>