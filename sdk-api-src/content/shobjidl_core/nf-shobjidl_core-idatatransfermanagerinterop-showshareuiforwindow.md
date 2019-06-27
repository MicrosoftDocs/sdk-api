---
UID: NF:shobjidl_core.IDataTransferManagerInterop.ShowShareUIForWindow
title: IDataTransferManagerInterop::ShowShareUIForWindow (shobjidl_core.h)
author: windows-sdk-content
description: Displays the UI for sharing content for the specified window.
old-location: shell\idatatransfermanagerinterop_showshareuiforwindow.htm
tech.root: shell
ms.assetid: 095AE176-5EA1-470E-AA4A-ACD91AF54E5D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDataTransferManagerInterop interface [Windows Shell],ShowShareUIForWindow method, IDataTransferManagerInterop.ShowShareUIForWindow, IDataTransferManagerInterop::ShowShareUIForWindow, ShowShareUIForWindow, ShowShareUIForWindow method [Windows Shell], ShowShareUIForWindow method [Windows Shell],IDataTransferManagerInterop interface, shell.idatatransfermanagerinterop_showshareuiforwindow, shobjidl_core/IDataTransferManagerInterop::ShowShareUIForWindow
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IDataTransferManagerInterop.ShowShareUIForWindow"
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [UWP apps only]
req.target-min-winversvr: Windows Server 2012 [UWP apps only]
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
 - IDataTransferManagerInterop.ShowShareUIForWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataTransferManagerInterop::ShowShareUIForWindow


## -description


Displays the UI for sharing content for the specified window.


## -parameters




### -param appWindow [in]

The window to show the share UI for.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is equivalent to the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.applicationmodel.datatransfer.datatransfermanager.showshareui">DataTransferManager.ShowShareUI</a> method, except that you specify a window from a multi-window Windows Store app.




## -see-also




<a href="https://docs.microsoft.com/en-us/uwp/api/windows.applicationmodel.datatransfer.datatransfermanager">DataTransferManager</a>



<a href="https://docs.microsoft.com/en-us/uwp/api/windows.applicationmodel.datatransfer.datatransfermanager.showshareui">DataTransferManager.ShowShareUI</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idatatransfermanagerinterop">IDataTransferManagerInterop</a>
 

 

