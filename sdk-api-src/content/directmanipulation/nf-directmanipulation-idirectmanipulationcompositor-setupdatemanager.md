---
UID: NF:directmanipulation.IDirectManipulationCompositor.SetUpdateManager
title: IDirectManipulationCompositor::SetUpdateManager (directmanipulation.h)
author: windows-sdk-content
description: Sets the update manager used to send compositor updates to Direct Manipulation.
old-location: directmanipulation\idirectmanipulationcompositor_setupdatemanager.htm
tech.root: directmanipulation
ms.assetid: 8efab95b-2e06-4a3f-9b1b-171c1aada40a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectManipulationCompositor interface [Direct Manipulation],SetUpdateManager method, IDirectManipulationCompositor.SetUpdateManager, IDirectManipulationCompositor::SetUpdateManager, SetUpdateManager, SetUpdateManager method [Direct Manipulation], SetUpdateManager method [Direct Manipulation],IDirectManipulationCompositor interface, directmanipulation.idirectmanipulationcompositor_setupdatemanager, directmanipulation/IDirectManipulationCompositor::SetUpdateManager
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
 - IDirectManipulationCompositor.SetUpdateManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationCompositor::SetUpdateManager


## -description



    Sets the update manager used to send compositor updates to <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>. 




## -parameters




### -param updateManager [in]

The <a href="https://msdn.microsoft.com/30626a22-1ded-49ff-a6c3-619a14d5ee3b">update manager</a>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Retrieve <i>updateManager</i>  by calling <a href="https://msdn.microsoft.com/f3080fcb-3bbe-492b-a94e-322f93781cf5">GetUpdateManager</a>.

Call this method during <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> initialization to connect the compositor to the <i>update manager</i>.




## -see-also




<a href="https://msdn.microsoft.com/b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1">IDirectManipulationCompositor</a>
 

 

