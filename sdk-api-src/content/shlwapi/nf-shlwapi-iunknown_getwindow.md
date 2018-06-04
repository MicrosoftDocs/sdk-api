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

# IUnknown_GetWindow function


## -description


Attempts to retrieve a window handle from a Component Object Model (COM) object by querying for various interfaces that have a <b>GetWindow</b> method.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the COM object from which this function will attempt to obtain a window handle.


### -param phwnd [out]

Type: <b>HWND*</b>

A pointer to a HWND that, when this function returns successfully, receives the window handle. If a window handle was not obtained, this parameter is set to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if a window handle was successfully returned, or a COM error code otherwise. If no suitable interface was found, the function returns E_NOINTERFACE. Otherwise, the function returns the <b>HRESULT</b> returned by the corresponding interface's <b>GetWindow</b> method.




## -remarks



This function attempts to retrieve the window handle by calling <a href="https://msdn.microsoft.com/833adc81-be58-44a1-88f1-9aa28808e67b">IOleWindow::GetWindow</a>, <a href="ie.IInternetSecurityMgrSite_GetWindow_Method">IInternetSecurityMgrSite::GetWindow</a>, and <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView::GetWindow</a>. It is possible that future versions of <b>IUnknown_GetWindow</b> may attempt additional interfaces.

<div class="alert"><b>Note</b>  The query for <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> is theoretically unnecessary because <b>IShellView</b> derives from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. The function explicitly queries for this interface because some objects implement <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> incorrectly and fail to respond to a query for the base interface.</div>
<div> </div>


