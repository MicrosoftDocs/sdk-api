---
UID: NF:shobjidl_core.IExplorerBrowser.GetCurrentView
title: IExplorerBrowser::GetCurrentView
author: windows-sdk-content
description: Gets an interface for the current view of the browser.
old-location: shell\IExplorerBrowser_GetCurrentView.htm
tech.root: Shell
ms.assetid: e7c05a67-f739-487d-872a-3598b790d5c9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetCurrentView, GetCurrentView method [Windows Shell], GetCurrentView method [Windows Shell],IExplorerBrowser interface, IExplorerBrowser interface [Windows Shell],GetCurrentView method, IExplorerBrowser.GetCurrentView, IExplorerBrowser::GetCurrentView, _shell_IExplorerBrowser_GetCurrentView, shell.IExplorerBrowser_GetCurrentView, shobjidl_core/IExplorerBrowser::GetCurrentView
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
 - IExplorerBrowser.GetCurrentView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

When this method returns, contains the interface pointer requested in <i>riid</i>. This will typically be <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>, <a href="https://msdn.microsoft.com/a61aec39-406d-4066-941d-e788d64f4310">IShellView2</a>, <a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>, or a related interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use the <b>IID_PPV_ARGS</b> macro.



