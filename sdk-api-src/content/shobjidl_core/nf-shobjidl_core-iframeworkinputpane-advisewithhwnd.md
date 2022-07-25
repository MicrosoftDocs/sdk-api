---
UID: NF:shobjidl_core.IFrameworkInputPane.AdviseWithHWND
title: IFrameworkInputPane::AdviseWithHWND (shobjidl_core.h)
description: Registers the app's input pane handler object to receive notifications on behalf of a window when an event triggers the input pane. This method differs from Advise in that it references its window through an HWND.
helpviewer_keywords: ["AdviseWithHWND","AdviseWithHWND method [Windows Shell]","AdviseWithHWND method [Windows Shell]","IFrameworkInputPane interface","IFrameworkInputPane interface [Windows Shell]","AdviseWithHWND method","IFrameworkInputPane.AdviseWithHWND","IFrameworkInputPane::AdviseWithHWND","shell.IFrameworkInputPane_AdviseWithHWND","shobjidl_core/IFrameworkInputPane::AdviseWithHWND"]
old-location: shell\IFrameworkInputPane_AdviseWithHWND.htm
tech.root: shell
ms.assetid: 6C4F52DC-0ED0-4A2D-9C5F-F29063E1AAEE
ms.date: 12/05/2018
ms.keywords: AdviseWithHWND, AdviseWithHWND method [Windows Shell], AdviseWithHWND method [Windows Shell],IFrameworkInputPane interface, IFrameworkInputPane interface [Windows Shell],AdviseWithHWND method, IFrameworkInputPane.AdviseWithHWND, IFrameworkInputPane::AdviseWithHWND, shell.IFrameworkInputPane_AdviseWithHWND, shobjidl_core/IFrameworkInputPane::AdviseWithHWND
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
 - IFrameworkInputPane::AdviseWithHWND
 - shobjidl_core/IFrameworkInputPane::AdviseWithHWND
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
 - IFrameworkInputPane.AdviseWithHWND
---

# IFrameworkInputPane::AdviseWithHWND


## -description

Registers the app's input pane handler object to receive notifications on behalf of a window when an event triggers the input pane. This method differs from <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-advise">Advise</a> in that it references its window through an <b>HWND</b>.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The handle of the window for which the handler should listen for input pane events.

### -param pHandler [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpanehandler">IFrameworkInputPaneHandler</a>*</b>

An <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpanehandler">IFrameworkInputPaneHandler</a> interface pointer to the handler instance for this app.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a value that, when this method returns successfully, receives a cookie for that can be used later to unregister the handler through the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-unadvise">Unadvise</a> method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpane">IFrameworkInputPane</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-advise">IFrameworkInputPane::Advise</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-unadvise">IFrameworkInputPane::Unadvise</a>