---
UID: NF:directmanipulation.IDirectManipulationUpdateManager.Update
title: IDirectManipulationUpdateManager::Update
author: windows-sdk-content
description: Updates Direct Manipulation at the current time.
old-location: directmanipulation\idirectmanipulationupdatemanager_update.htm
old-project: directmanipulation
ms.assetid: dffa747c-933a-4b61-9f15-e175d9338774
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDirectManipulationUpdateManager interface [Direct Manipulation],Update method, IDirectManipulationUpdateManager.Update, IDirectManipulationUpdateManager::Update, Update, Update method [Direct Manipulation], Update method [Direct Manipulation],IDirectManipulationUpdateManager interface, directmanipulation.idirectmanipulationupdatemanager_update, directmanipulation/IDirectManipulationUpdateManager::Update
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
 - IDirectManipulationUpdateManager.Update
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationUpdateManager::Update


## -description


Updates <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> at the current time.


## -parameters




### -param frameInfo [in, optional]

The frame info provider used to predict the position of the content and compensate for latency during composition.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the application provides its own implementation of <a href="https://msdn.microsoft.com/b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1">IDirectManipulationCompositor</a>, this implementation should call <b>Update</b> whenever there is a compositor update. Frame timing information can be provided to <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> through the <a href="https://msdn.microsoft.com/15B7CA2A-DEC3-479B-BD41-38A57037002F">IDirectManipulationFrameInfoProvider</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/30626a22-1ded-49ff-a6c3-619a14d5ee3b">IDirectManipulationUpdateManager</a>
 

 

