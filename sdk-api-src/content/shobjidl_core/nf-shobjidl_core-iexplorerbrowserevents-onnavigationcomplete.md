---
UID: NF:shobjidl_core.IExplorerBrowserEvents.OnNavigationComplete
title: IExplorerBrowserEvents::OnNavigationComplete
author: windows-sdk-content
description: Notifies clients that the Explorer browser has successfully navigated to a Shell folder.
old-location: shell\IExplorerBrowserEvents_OnNavigationComplete.htm
tech.root: shell
ms.assetid: 54c97a55-a8d1-4635-a1e0-2f92d52ddc10
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IExplorerBrowserEvents interface [Windows Shell],OnNavigationComplete method, IExplorerBrowserEvents.OnNavigationComplete, IExplorerBrowserEvents::OnNavigationComplete, OnNavigationComplete, OnNavigationComplete method [Windows Shell], OnNavigationComplete method [Windows Shell],IExplorerBrowserEvents interface, _shell_IExplorerBrowserEvents_OnNavigationComplete, shell.IExplorerBrowserEvents_OnNavigationComplete, shobjidl_core/IExplorerBrowserEvents::OnNavigationComplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerBrowserEvents.OnNavigationComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called after method <a href="https://msdn.microsoft.com/801d59f5-6e92-4e3c-938a-e94b43b7c6f1">IExplorerBrowserEvents::OnViewCreated</a>, assuming a successful view creation.

After a navigation and view creation, either <b>IExplorerBrowserEvents::OnNavigationComplete</b> or <a href="https://msdn.microsoft.com/d4de3b81-4482-47c8-bb47-593aba484952">IExplorerBrowserEvents::OnNavigationFailed</a> is called depending on whether the destination could be navigated to. For example, a failure to navigate includes a destination that is not reached either because there is no route to the path or the user has canceled.
            



