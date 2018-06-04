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

# IPlayToManagerInterop::GetForWindow


## -description


Gets the <a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a> instance for the specified window.


## -parameters




### -param appWindow [in]

The window to get the <a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a> instance for.


### -param riid [in]

The reference ID of the specified window.


### -param playToManager [out, retval]

The <a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a> instance for the specified window.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use the <b>GetForWindow</b> method to get the <a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a> for the specified window. The <b>GetForWindow</b> method is equivalent to the <a href="https://msdn.microsoft.com/8b707202-fb49-4e3e-885c-a37d17211487">GetForCurrentView</a> method, except that you supply a reference to a window from a multi-window Windows Store app.




## -see-also




<a href="https://msdn.microsoft.com/8b707202-fb49-4e3e-885c-a37d17211487">GetForCurrentView</a>



<a href="https://msdn.microsoft.com/e7a8df61-e5ae-4eff-a4eb-e0a5cdae3b7f">IPlayToManagerInterop</a>



<a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a>
 

 

