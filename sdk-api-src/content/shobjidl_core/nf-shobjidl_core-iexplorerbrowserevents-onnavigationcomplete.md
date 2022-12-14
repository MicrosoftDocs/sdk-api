---
UID: NF:shobjidl_core.IExplorerBrowserEvents.OnNavigationComplete
title: IExplorerBrowserEvents::OnNavigationComplete (shobjidl_core.h)
description: Notifies clients that the Explorer browser has successfully navigated to a Shell folder.
helpviewer_keywords: ["IExplorerBrowserEvents interface [Windows Shell]","OnNavigationComplete method","IExplorerBrowserEvents.OnNavigationComplete","IExplorerBrowserEvents::OnNavigationComplete","OnNavigationComplete","OnNavigationComplete method [Windows Shell]","OnNavigationComplete method [Windows Shell]","IExplorerBrowserEvents interface","_shell_IExplorerBrowserEvents_OnNavigationComplete","shell.IExplorerBrowserEvents_OnNavigationComplete","shobjidl_core/IExplorerBrowserEvents::OnNavigationComplete"]
old-location: shell\IExplorerBrowserEvents_OnNavigationComplete.htm
tech.root: shell
ms.assetid: 54c97a55-a8d1-4635-a1e0-2f92d52ddc10
ms.date: 12/05/2018
ms.keywords: IExplorerBrowserEvents interface [Windows Shell],OnNavigationComplete method, IExplorerBrowserEvents.OnNavigationComplete, IExplorerBrowserEvents::OnNavigationComplete, OnNavigationComplete, OnNavigationComplete method [Windows Shell], OnNavigationComplete method [Windows Shell],IExplorerBrowserEvents interface, _shell_IExplorerBrowserEvents_OnNavigationComplete, shell.IExplorerBrowserEvents_OnNavigationComplete, shobjidl_core/IExplorerBrowserEvents::OnNavigationComplete
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
 - IExplorerBrowserEvents::OnNavigationComplete
 - shobjidl_core/IExplorerBrowserEvents::OnNavigationComplete
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
 - IExplorerBrowserEvents.OnNavigationComplete
---

# IExplorerBrowserEvents::OnNavigationComplete


## -description

Notifies clients that the Explorer browser has successfully navigated to a Shell folder.

## -parameters

### -param pidlFolder [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL that specifies the folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called after method <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onviewcreated">IExplorerBrowserEvents::OnViewCreated</a>, assuming a successful view creation.

After a navigation and view creation, either <b>IExplorerBrowserEvents::OnNavigationComplete</b> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationfailed">IExplorerBrowserEvents::OnNavigationFailed</a> is called depending on whether the destination could be navigated to. For example, a failure to navigate includes a destination that is not reached either because there is no route to the path or the user has canceled.