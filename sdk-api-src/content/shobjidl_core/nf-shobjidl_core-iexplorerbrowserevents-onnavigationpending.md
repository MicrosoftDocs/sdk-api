---
UID: NF:shobjidl_core.IExplorerBrowserEvents.OnNavigationPending
title: IExplorerBrowserEvents::OnNavigationPending
author: windows-sdk-content
description: Notifies clients of a pending Explorer browser navigation to a Shell folder.
old-location: shell\IExplorerBrowserEvents_OnNavigationPending.htm
old-project: shell
ms.assetid: 52dfb901-ee65-444a-8b27-2d2811cf83c0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IExplorerBrowserEvents interface [Windows Shell],OnNavigationPending method, IExplorerBrowserEvents.OnNavigationPending, IExplorerBrowserEvents::OnNavigationPending, OnNavigationPending, OnNavigationPending method [Windows Shell], OnNavigationPending method [Windows Shell],IExplorerBrowserEvents interface, _shell_IExplorerBrowserEvents_OnNavigationPending, shell.IExplorerBrowserEvents_OnNavigationPending, shobjidl_core/IExplorerBrowserEvents::OnNavigationPending
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IExplorerBrowserEvents.OnNavigationPending
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Explorer browser calls this method before it navigates to a folder, that is, before calling <a href="https://msdn.microsoft.com/d4de3b81-4482-47c8-bb47-593aba484952">IExplorerBrowserEvents::OnNavigationFailed</a> or  <a href="https://msdn.microsoft.com/54c97a55-a8d1-4635-a1e0-2f92d52ddc10">IExplorerBrowserEvents::OnNavigationComplete</a>.


Returning any failure code from this method, including E_NOTIMPL, will cancel the navigation.



