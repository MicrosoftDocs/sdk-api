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

# IUIAnimationLoopIterationChangeHandler2::OnLoopIterationChanged


## -description


Handles loop iteration change events, which occur when a loop within a storyboard begins a new iteration.


## -parameters




### -param storyboard [in]

The storyboard to which the loop belongs.


### -param id [in]

The loop ID.


### -param newIterationCount [in]

The iteration count for the latest <a href="https://msdn.microsoft.com/5735ABDB-E1AE-41C0-9F37-92084CEF6FAD">IUIAnimationManager2::Update</a>.


### -param oldIterationCount [in]

The iteration count for the previous <a href="https://msdn.microsoft.com/5735ABDB-E1AE-41C0-9F37-92084CEF6FAD">IUIAnimationManager2::Update</a>.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/DB3995BA-856F-407D-AA89-247D84C3F7A1">IUIAnimationLoopIterationChangeHandler2</a>
 

 

