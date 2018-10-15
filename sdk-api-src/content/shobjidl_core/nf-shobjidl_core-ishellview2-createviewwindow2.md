---
UID: NF:shobjidl_core.IShellView2.CreateViewWindow2
title: IShellView2::CreateViewWindow2
author: windows-sdk-content
description: Used to request the creation of a new Shell view window. It can be either the right pane of Windows Explorer or the client window of a folder window.
old-location: shell\IShellView2_CreateViewWindow2.htm
tech.root: shell
ms.assetid: 3b829f5f-26ea-4987-be05-6725eeff5fed
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CreateViewWindow2, CreateViewWindow2 method [Windows Shell], CreateViewWindow2 method [Windows Shell],IShellView2 interface, IShellView2 interface [Windows Shell],CreateViewWindow2 method, IShellView2.CreateViewWindow2, IShellView2::CreateViewWindow2, _win32_IShellView2_CreateViewWindow2, shell.IShellView2_CreateViewWindow2, shobjidl_core/IShellView2::CreateViewWindow2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellView2.CreateViewWindow2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellView2::CreateViewWindow2


## -description


Used to request the creation of a new Shell view window. It can be either the right pane of Windows Explorer or the client window of a folder window.


## -parameters




### -param lpParams

Type: <b>LPSV2CVW2_PARAMS</b>

A pointer to an <a href="https://msdn.microsoft.com/7e165654-74ea-4d8b-81b7-11257f87af53">SV2CVW2_PARAMS</a> structure that defines the new view window.


## -returns



Type: <b>HRESULT</b>

Returns a success code if successful, or a COM error code otherwise. Use the <a href="com.succeeded">SUCCEEDED</a> and <a href="com.failed">FAILED</a> macros to determine whether the operation succeeded or failed.




## -remarks



This method supersedes <a href="https://msdn.microsoft.com/62d71bca-d2cb-4668-b0bf-2e53756f2cd9">CreateViewWindow</a>. With <b>CreateViewWindow2</b>, developers are not restricted to the standard view modes provided by <b>CreateViewWindow</b>, but may also create their own. All view modes are now identified by their GUID.

The size of the structure, previous view window, folder settings, parent Shell browser, and view rectangle are passed into <b>IShellView2::CreateViewWindow2</b> in the first five members of <i>lpParams</i>. The method is responsible for creating the new window and passing back its window handle and the GUID of the view mode in the last two parameters. <b>IShellView2::CreateViewWindow2</b> should call the parent browser's <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IShellBrowser::AddRef</a> method and store the interface pointer. It can be used for communication with the Windows Explorer window.




## -see-also




<a href="https://msdn.microsoft.com/a61aec39-406d-4066-941d-e788d64f4310">IShellView2</a>



<a href="https://msdn.microsoft.com/74fe42fe-33de-483a-88e4-50da9c1f77c2">IShellView2::GetView</a>
 

 

