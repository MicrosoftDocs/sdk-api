---
UID: NF:shobjidl_core.IExplorerBrowserEvents.OnViewCreated
title: IExplorerBrowserEvents::OnViewCreated
author: windows-sdk-content
description: Notifies clients that the view of the Explorer browser has been created and can be modified.
old-location: shell\IExplorerBrowserEvents_OnViewCreated.htm
old-project: shell
ms.assetid: 801d59f5-6e92-4e3c-938a-e94b43b7c6f1
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IExplorerBrowserEvents interface [Windows Shell],OnViewCreated method, IExplorerBrowserEvents.OnViewCreated, IExplorerBrowserEvents::OnViewCreated, OnViewCreated, OnViewCreated method [Windows Shell], OnViewCreated method [Windows Shell],IExplorerBrowserEvents interface, _shell_IExplorerBrowserEvents_OnViewCreated, shell.IExplorerBrowserEvents_OnViewCreated, shobjidl_core/IExplorerBrowserEvents::OnViewCreated
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerBrowserEvents.OnViewCreated
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IExplorerBrowserEvents::OnViewCreated


## -description


Notifies clients that the view of the Explorer browser has been created and can be modified.


## -parameters




### -param psv [in]

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An Explorer browser calls this method to enable the client to perform any modifications to the Explorer browser view before it is shown; for example, to set view modes or folder flags.



