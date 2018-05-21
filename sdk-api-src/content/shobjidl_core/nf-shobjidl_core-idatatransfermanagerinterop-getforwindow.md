---
UID: NF:shobjidl_core.IDataTransferManagerInterop.GetForWindow
title: IDataTransferManagerInterop::GetForWindow
author: windows-driver-content
description: Gets the DataTransferManager instance for the specified window.
old-location: shell\idatatransfermanagerinterop_getforwindow.htm
old-project: shell
ms.assetid: 129CEEBF-0D02-4746-8F9B-4F5F5A95E6A2
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetForWindow, GetForWindow method [Windows Shell], GetForWindow method [Windows Shell],IDataTransferManagerInterop interface, IDataTransferManagerInterop interface [Windows Shell],GetForWindow method, IDataTransferManagerInterop.GetForWindow, IDataTransferManagerInterop::GetForWindow, shell.idatatransfermanagerinterop_getforwindow, shobjidl_core/IDataTransferManagerInterop::GetForWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IDataTransferManagerInterop.GetForWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IDataTransferManagerInterop::GetForWindow


## -description


Gets the <a href="https://msdn.microsoft.com/21a12246-a49e-4f1e-b539-c35164b488d7">DataTransferManager</a> instance for the specified window.


## -parameters




### -param appWindow [in]

The window whose <a href="https://msdn.microsoft.com/21a12246-a49e-4f1e-b539-c35164b488d7">DataTransferManager</a> instance is to be retrieved.


### -param riid [in]

The requested interface ID of the <a href="https://msdn.microsoft.com/21a12246-a49e-4f1e-b539-c35164b488d7">DataTransferManager</a> instance.


### -param dataTransferManager [out, optional]

Receives the <a href="https://msdn.microsoft.com/21a12246-a49e-4f1e-b539-c35164b488d7">DataTransferManager</a> instance.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is equivalent to the <a href="https://msdn.microsoft.com/f0361277-be0e-4a30-9be4-9e861e7b73cf">DataTransferManager.GetForCurrentView</a> method, except that you specify a window from a multi-window Windows Store app.




## -see-also




<a href="https://msdn.microsoft.com/21a12246-a49e-4f1e-b539-c35164b488d7">DataTransferManager</a>



<a href="https://msdn.microsoft.com/f0361277-be0e-4a30-9be4-9e861e7b73cf">DataTransferManager.GetForCurrentView</a>



<a href="https://msdn.microsoft.com/C4F49401-C863-4D3B-80EE-D36F714E7D90">IDataTransferManagerInterop</a>
 

 

