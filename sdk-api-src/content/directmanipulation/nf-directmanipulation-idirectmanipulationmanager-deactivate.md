---
UID: NF:directmanipulation.IDirectManipulationManager.Deactivate
title: IDirectManipulationManager::Deactivate
author: windows-sdk-content
description: Deactivates Direct Manipulation for processing input and handling callbacks on the specified window.
old-location: directmanipulation\idirectmanipulationmanager_deactivate.htm
tech.root: directmanipulation
ms.assetid: 7f80fe8a-e088-41fa-b72e-2b248307ac4a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Deactivate, Deactivate method [Direct Manipulation], Deactivate method [Direct Manipulation],IDirectManipulationManager interface, IDirectManipulationManager interface [Direct Manipulation],Deactivate method, IDirectManipulationManager.Deactivate, IDirectManipulationManager::Deactivate, directmanipulation.idirectmanipulationmanager_deactivate, directmanipulation/IDirectManipulationManager::Deactivate
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - DirectManipulation.h
api_name:
 - IDirectManipulationManager.Deactivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

