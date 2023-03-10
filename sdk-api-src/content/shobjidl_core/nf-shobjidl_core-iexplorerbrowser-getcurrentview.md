---
UID: NF:shobjidl_core.IExplorerBrowser.GetCurrentView
title: IExplorerBrowser::GetCurrentView (shobjidl_core.h)
description: Gets an interface for the current view of the browser.
helpviewer_keywords: ["GetCurrentView","GetCurrentView method [Windows Shell]","GetCurrentView method [Windows Shell]","IExplorerBrowser interface","IExplorerBrowser interface [Windows Shell]","GetCurrentView method","IExplorerBrowser.GetCurrentView","IExplorerBrowser::GetCurrentView","_shell_IExplorerBrowser_GetCurrentView","shell.IExplorerBrowser_GetCurrentView","shobjidl_core/IExplorerBrowser::GetCurrentView"]
old-location: shell\IExplorerBrowser_GetCurrentView.htm
tech.root: shell
ms.assetid: e7c05a67-f739-487d-872a-3598b790d5c9
ms.date: 12/05/2018
ms.keywords: GetCurrentView, GetCurrentView method [Windows Shell], GetCurrentView method [Windows Shell],IExplorerBrowser interface, IExplorerBrowser interface [Windows Shell],GetCurrentView method, IExplorerBrowser.GetCurrentView, IExplorerBrowser::GetCurrentView, _shell_IExplorerBrowser_GetCurrentView, shell.IExplorerBrowser_GetCurrentView, shobjidl_core/IExplorerBrowser::GetCurrentView
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IExplorerBrowser::GetCurrentView
 - shobjidl_core/IExplorerBrowser::GetCurrentView
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
 - IExplorerBrowser.GetCurrentView
---

# IExplorerBrowser::GetCurrentView


## -description

Gets an interface for the current view of the browser.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired interface ID.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This will typically be <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2">IShellView2</a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>, or a related interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use the <b>IID_PPV_ARGS</b> macro.