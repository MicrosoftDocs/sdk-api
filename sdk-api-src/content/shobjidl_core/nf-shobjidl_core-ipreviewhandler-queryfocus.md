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

# IPreviewHandler::QueryFocus


## -description


Directs the preview handler to return the <b>HWND</b> from calling the <a href="https://msdn.microsoft.com/3929771f-0402-4554-8e39-f945cd77b16d">GetFocus Function</a>.


## -parameters




### -param phwnd [out]

Type: <b>HWND*</b>

When this method returns, contains a pointer to the HWND returned from calling the <a href="https://msdn.microsoft.com/3929771f-0402-4554-8e39-f945cd77b16d">GetFocus Function</a> from the preview handler's foreground thread.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is necessary because <a href="https://msdn.microsoft.com/3929771f-0402-4554-8e39-f945cd77b16d">GetFocus Function</a> can only succeed if the focus is on a window created by the calling thread. This method is used by the host to manage the tabbing order and to support tabbing into and out of the preview handler's windows.



