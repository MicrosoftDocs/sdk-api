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

# IDirectManipulationManager::Deactivate


## -description


Deactivates <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> for processing input and  handling callbacks on the specified window. 


## -parameters




### -param window [in]

The window in which to deactivate input.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The manipulation manager is deactivated by default. The manager does not receive or respond to input until <a href="https://msdn.microsoft.com/49a5eccd-16a9-4dca-af78-224fd5acb611">Activate</a> is called. The manipulation manager should be deactivated when the app does not receive or respond to input. For example, when the app is minimized.

Calls to <a href="https://msdn.microsoft.com/49a5eccd-16a9-4dca-af78-224fd5acb611">Activate</a> and <b>Deactivate</b> are reference counted.





## -see-also




<a href="https://msdn.microsoft.com/d730a446-984e-4be0-aa7f-6d3dc93b2e34">IDirectManipulationManager</a>
 

 

