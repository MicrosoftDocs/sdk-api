---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

