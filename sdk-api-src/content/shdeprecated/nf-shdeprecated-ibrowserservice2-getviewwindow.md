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

# IBrowserService2::GetViewWindow


## -description


Deprecated. Provides direct access to the browser view window created by <a href="https://msdn.microsoft.com/f5e7f18b-86b3-4a30-bbb0-8c7f615c7186">IBrowserService2::CreateViewWindow</a>.


## -parameters




### -param phwndView [out]

Type: <b>HWND*</b>

A pointer to the handle of the browser window.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IBrowserService2::GetViewWindow</b> retrieves the same handle as found in the <b>_hwndView</b> member of the <a href="https://msdn.microsoft.com/d56e42e8-a556-4470-82d9-466edd84214f">BASEBROWSERDATA</a> structure. This method simply provides direct access to that view, bypassing the need to access the <b>BASEBROWSERDATA</b> structure though a method such as <a href="https://msdn.microsoft.com/60a9bbd1-5c11-4c6a-bae2-b85979ab8bda">IBrowserService2::GetBaseBrowserData</a>.



