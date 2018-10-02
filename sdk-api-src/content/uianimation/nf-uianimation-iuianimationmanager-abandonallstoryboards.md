---
UID: NF:uianimation.IUIAnimationManager.AbandonAllStoryboards
title: IUIAnimationManager::AbandonAllStoryboards
author: windows-sdk-content
description: Abandons all active storyboards.
old-location: uianimation\iuianimationmanager_abandonallstoryboards.htm
tech.root: UIAnimation
ms.assetid: cecb0026-ed6f-48b8-9381-d020a36e7e87
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AbandonAllStoryboards, AbandonAllStoryboards method [Windows Animation], AbandonAllStoryboards method [Windows Animation],IUIAnimationManager interface, IUIAnimationManager interface [Windows Animation],AbandonAllStoryboards method, IUIAnimationManager.AbandonAllStoryboards, IUIAnimationManager::AbandonAllStoryboards, uianimation.iuianimationmanager_abandonallstoryboards, uianimation/IUIAnimationManager::AbandonAllStoryboards
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAnimation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationManager.AbandonAllStoryboards
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationManager::AbandonAllStoryboards


## -description


Abandons all active storyboards.


## -parameters






## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Calling this method is equivalent to calling the <a href="https://msdn.microsoft.com/2350dbd0-3a67-4832-94dd-56adce80a387">IUIAnimationStoryboard::Abandon</a>method for each active storyboard.
         
         A storyboard is considered active if its status is <b>UI_ANIMATION_STORYBOARD_PLAYING</b> 
         or <b>UI_ANIMATION_STORYBOARD_SCHEDULED</b>.




## -see-also




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>



<a href="https://msdn.microsoft.com/2350dbd0-3a67-4832-94dd-56adce80a387">IUIAnimationStoryboard::Abandon</a>



<a href="https://msdn.microsoft.com/8ee9a17f-c57c-49df-950d-491e05ba8768">IUIAnimationStoryboard::GetStatus</a>



<a href="https://msdn.microsoft.com/02830092-0070-44dc-8db2-239941134473">UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

