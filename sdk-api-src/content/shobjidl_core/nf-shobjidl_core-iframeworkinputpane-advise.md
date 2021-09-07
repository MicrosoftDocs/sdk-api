---
UID: NF:shobjidl_core.IFrameworkInputPane.Advise
title: IFrameworkInputPane::Advise (shobjidl_core.h)
description: Registers the app's input pane handler object to receive notifications on behalf of a window when an event triggers the input pane. This method differs from AdviseWithHWND in that it references its window through an object that implements ICoreWindow.
helpviewer_keywords: ["Advise","Advise method [Windows Shell]","Advise method [Windows Shell]","IFrameworkInputPane interface","IFrameworkInputPane interface [Windows Shell]","Advise method","IFrameworkInputPane.Advise","IFrameworkInputPane::Advise","shell.IFrameworkInputPane_Advise","shobjidl_core/IFrameworkInputPane::Advise"]
old-location: shell\IFrameworkInputPane_Advise.htm
tech.root: shell
ms.assetid: F05A097F-13A4-48ad-B660-5B2409BB6D61
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],IFrameworkInputPane interface, IFrameworkInputPane interface [Windows Shell],Advise method, IFrameworkInputPane.Advise, IFrameworkInputPane::Advise, shell.IFrameworkInputPane_Advise, shobjidl_core/IFrameworkInputPane::Advise
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
 - IFrameworkInputPane::Advise
 - shobjidl_core/IFrameworkInputPane::Advise
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
 - IFrameworkInputPane.Advise
---

# IFrameworkInputPane::Advise


## -description

Registers the app's input pane handler object to receive notifications on behalf of a window when an event triggers the input pane. This method differs from <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-advisewithhwnd">AdviseWithHWND</a> in that it references its window through an object that implements <a href="/uwp/api/windows.ui.core.icorewindow">ICoreWindow</a>.

## -parameters

### -param pWindow [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the window (an object that implements <a href="/uwp/api/windows.ui.core.icorewindow">ICoreWindow</a>) for which the handler should listen for input pane events.

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



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-advisewithhwnd">IFrameworkInputPane::AdviseWithHWND</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-unadvise">IFrameworkInputPane::Unadvise</a>