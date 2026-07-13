---
UID: NF:shobjidl_core.IExplorerBrowserEvents.OnNavigationPending
title: IExplorerBrowserEvents::OnNavigationPending (shobjidl_core.h)
description: Notifies clients of a pending Explorer browser navigation to a Shell folder.
helpviewer_keywords: ["IExplorerBrowserEvents interface [Windows Shell]","OnNavigationPending method","IExplorerBrowserEvents.OnNavigationPending","IExplorerBrowserEvents::OnNavigationPending","OnNavigationPending","OnNavigationPending method [Windows Shell]","OnNavigationPending method [Windows Shell]","IExplorerBrowserEvents interface","_shell_IExplorerBrowserEvents_OnNavigationPending","shell.IExplorerBrowserEvents_OnNavigationPending","shobjidl_core/IExplorerBrowserEvents::OnNavigationPending"]
old-location: shell\IExplorerBrowserEvents_OnNavigationPending.htm
tech.root: shell
ms.assetid: 52dfb901-ee65-444a-8b27-2d2811cf83c0
ms.date: 12/05/2018
ms.keywords: IExplorerBrowserEvents interface [Windows Shell],OnNavigationPending method, IExplorerBrowserEvents.OnNavigationPending, IExplorerBrowserEvents::OnNavigationPending, OnNavigationPending, OnNavigationPending method [Windows Shell], OnNavigationPending method [Windows Shell],IExplorerBrowserEvents interface, _shell_IExplorerBrowserEvents_OnNavigationPending, shell.IExplorerBrowserEvents_OnNavigationPending, shobjidl_core/IExplorerBrowserEvents::OnNavigationPending
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
 - IExplorerBrowserEvents::OnNavigationPending
 - shobjidl_core/IExplorerBrowserEvents::OnNavigationPending
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
 - IExplorerBrowserEvents.OnNavigationPending
---

# IExplorerBrowserEvents::OnNavigationPending


## -description

Notifies clients of a pending Explorer browser navigation to a Shell folder.

## -parameters

### -param pidlFolder [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL that specifies the folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Explorer browser calls this method before it navigates to a folder, that is, before calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationfailed">IExplorerBrowserEvents::OnNavigationFailed</a> or  <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationcomplete">IExplorerBrowserEvents::OnNavigationComplete</a>.


Returning any failure code from this method, including E_NOTIMPL, will cancel the navigation.