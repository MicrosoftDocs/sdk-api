---
UID: NF:shobjidl_core.IExplorerBrowserEvents.OnNavigationFailed
title: IExplorerBrowserEvents::OnNavigationFailed (shobjidl_core.h)
description: Notifies clients that the Explorer browser has failed to navigate to a Shell folder.
helpviewer_keywords: ["IExplorerBrowserEvents interface [Windows Shell]","OnNavigationFailed method","IExplorerBrowserEvents.OnNavigationFailed","IExplorerBrowserEvents::OnNavigationFailed","OnNavigationFailed","OnNavigationFailed method [Windows Shell]","OnNavigationFailed method [Windows Shell]","IExplorerBrowserEvents interface","_shell_IExplorerBrowserEvents_OnNavigationFailed","shell.IExplorerBrowserEvents_OnNavigationFailed","shobjidl_core/IExplorerBrowserEvents::OnNavigationFailed"]
old-location: shell\IExplorerBrowserEvents_OnNavigationFailed.htm
tech.root: shell
ms.assetid: d4de3b81-4482-47c8-bb47-593aba484952
ms.date: 12/05/2018
ms.keywords: IExplorerBrowserEvents interface [Windows Shell],OnNavigationFailed method, IExplorerBrowserEvents.OnNavigationFailed, IExplorerBrowserEvents::OnNavigationFailed, OnNavigationFailed, OnNavigationFailed method [Windows Shell], OnNavigationFailed method [Windows Shell],IExplorerBrowserEvents interface, _shell_IExplorerBrowserEvents_OnNavigationFailed, shell.IExplorerBrowserEvents_OnNavigationFailed, shobjidl_core/IExplorerBrowserEvents::OnNavigationFailed
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
 - IExplorerBrowserEvents::OnNavigationFailed
 - shobjidl_core/IExplorerBrowserEvents::OnNavigationFailed
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
 - IExplorerBrowserEvents.OnNavigationFailed
---

# IExplorerBrowserEvents::OnNavigationFailed


## -description

Notifies clients that the Explorer browser has failed to navigate to a Shell folder.

## -parameters

### -param pidlFolder [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL that specifies the folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called after method <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onviewcreated">IExplorerBrowserEvents::OnViewCreated</a>, assuming a successful view creation.

After a navigation and view creation, either <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationcomplete">IExplorerBrowserEvents::OnNavigationComplete</a> or <b>IExplorerBrowserEvents::OnNavigationFailed</b> is called, depending on whether the destination could be navigated to. For example, a failure to navigate includes a destination that is not reached either because there is no route to the path or the user has canceled.