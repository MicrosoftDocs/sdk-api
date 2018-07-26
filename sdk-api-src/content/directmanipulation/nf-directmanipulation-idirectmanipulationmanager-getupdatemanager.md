---
UID: NF:directmanipulation.IDirectManipulationManager.GetUpdateManager
title: IDirectManipulationManager::GetUpdateManager
author: windows-sdk-content
description: Gets a pointer to an IDirectManipulationUpdateManager object that receives compositor updates.
old-location: directmanipulation\idirectmanipulationmanager_getupdatemanager.htm
old-project: directmanipulation
ms.assetid: f3080fcb-3bbe-492b-a94e-322f93781cf5
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetUpdateManager, GetUpdateManager method [Direct Manipulation], GetUpdateManager method [Direct Manipulation],IDirectManipulationManager interface, IDirectManipulationManager interface [Direct Manipulation],GetUpdateManager method, IDirectManipulationManager.GetUpdateManager, IDirectManipulationManager::GetUpdateManager, directmanipulation.idirectmanipulationmanager_getupdatemanager, directmanipulation/IDirectManipulationManager::GetUpdateManager
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationManager.GetUpdateManager
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationManager::GetUpdateManager


## -description


Gets a pointer to an <a href="https://msdn.microsoft.com/30626a22-1ded-49ff-a6c3-619a14d5ee3b">IDirectManipulationUpdateManager</a> object that receives compositor updates. 


## -parameters




### -param riid [in]

IID to the interface.


### -param object [out, retval]

Pointer to the new <a href="https://msdn.microsoft.com/30626a22-1ded-49ff-a6c3-619a14d5ee3b">IDirectManipulationUpdateManager</a> object.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For the compositor to respond to update events from <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>, you must associate <a href="https://msdn.microsoft.com/30626a22-1ded-49ff-a6c3-619a14d5ee3b">IDirectManipulationUpdateManager</a> to an <a href="https://msdn.microsoft.com/b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1">IDirectManipulationCompositor</a> object during initialization. Use  <b>GetUpdateManager</b> to obtain a pointer to a <b>IDirectManipulationUpdateManager</b> object. Pass this pointer to the compositor using the <a href="https://msdn.microsoft.com/8efab95b-2e06-4a3f-9b1b-171c1aada40a">SetUpdateManager</a> method.




## -see-also




<a href="https://msdn.microsoft.com/d730a446-984e-4be0-aa7f-6d3dc93b2e34">IDirectManipulationManager</a>
 

 

