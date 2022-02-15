---
UID: NF:shobjidl_core.IDataTransferManagerInterop.GetForWindow
title: IDataTransferManagerInterop::GetForWindow (shobjidl_core.h)
description: Gets the DataTransferManager instance for the specified window.
helpviewer_keywords: ["GetForWindow","GetForWindow method [Windows Shell]","GetForWindow method [Windows Shell]","IDataTransferManagerInterop interface","IDataTransferManagerInterop interface [Windows Shell]","GetForWindow method","IDataTransferManagerInterop.GetForWindow","IDataTransferManagerInterop::GetForWindow","shell.idatatransfermanagerinterop_getforwindow","shobjidl_core/IDataTransferManagerInterop::GetForWindow"]
old-location: shell\idatatransfermanagerinterop_getforwindow.htm
tech.root: shell
ms.assetid: 129CEEBF-0D02-4746-8F9B-4F5F5A95E6A2
ms.date: 12/05/2018
ms.keywords: GetForWindow, GetForWindow method [Windows Shell], GetForWindow method [Windows Shell],IDataTransferManagerInterop interface, IDataTransferManagerInterop interface [Windows Shell],GetForWindow method, IDataTransferManagerInterop.GetForWindow, IDataTransferManagerInterop::GetForWindow, shell.idatatransfermanagerinterop_getforwindow, shobjidl_core/IDataTransferManagerInterop::GetForWindow
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataTransferManagerInterop::GetForWindow
 - shobjidl_core/IDataTransferManagerInterop::GetForWindow
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
 - IDataTransferManagerInterop.GetForWindow
---

# IDataTransferManagerInterop::GetForWindow


## -description

Gets the <a href="/uwp/api/windows.applicationmodel.datatransfer.datatransfermanager">DataTransferManager</a> instance for the specified window.

## -parameters

### -param appWindow [in]

The window whose <a href="/uwp/api/windows.applicationmodel.datatransfer.datatransfermanager">DataTransferManager</a> instance is to be retrieved.

### -param riid [in]

The requested interface ID of the <a href="/uwp/api/windows.applicationmodel.datatransfer.datatransfermanager">DataTransferManager</a> instance.

### -param dataTransferManager [out, optional]

Receives the <a href="/uwp/api/windows.applicationmodel.datatransfer.datatransfermanager">DataTransferManager</a> instance.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is equivalent to the <a href="/uwp/api/windows.applicationmodel.datatransfer.datatransfermanager.getforcurrentview">DataTransferManager.GetForCurrentView</a> method, except that you specify a window from a multi-window Windows Store app.

## -see-also

<a href="/uwp/api/windows.applicationmodel.datatransfer.datatransfermanager">DataTransferManager</a>



<a href="/uwp/api/windows.applicationmodel.datatransfer.datatransfermanager.getforcurrentview">DataTransferManager.GetForCurrentView</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idatatransfermanagerinterop">IDataTransferManagerInterop</a>