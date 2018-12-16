---
UID: NF:uianimation.IUIAnimationManager.FinishAllStoryboards
title: IUIAnimationManager::FinishAllStoryboards
author: windows-sdk-content
description: Finishes all active storyboards within the specified time interval.
old-location: uianimation\iuianimationmanager_finishallstoryboards.htm
tech.root: UIAnimation
ms.assetid: db5ba70c-3904-4053-881a-b1412beb35f3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FinishAllStoryboards, FinishAllStoryboards method [Windows Animation], FinishAllStoryboards method [Windows Animation],IUIAnimationManager interface, IUIAnimationManager interface [Windows Animation],FinishAllStoryboards method, IUIAnimationManager.FinishAllStoryboards, IUIAnimationManager::FinishAllStoryboards, uianimation.iuianimationmanager_finishallstoryboards, uianimation/IUIAnimationManager::FinishAllStoryboards
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
 - IUIAnimationManager.FinishAllStoryboards
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationManager::FinishAllStoryboards


## -description


Finishes all active storyboards within the specified time interval.


## -parameters




### -param completionDeadline [in]

The maximum time interval during which all storyboards must be finished.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Calling <b>FinishAllStoryboards</b> ensures that all active storyboards finish within the specified completion deadline. If a storyboard is scheduled to play past the deadline, it is compressed.
         
         A storyboard is considered active if its status is <b>UI_ANIMATION_STORYBOARD_PLAYING</b> 
         or <b>UI_ANIMATION_STORYBOARD_SCHEDULED</b>.




## -see-also




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>



<a href="https://msdn.microsoft.com/45d0872a-dbcf-4151-a880-80b2c6fb884c">IUIAnimationStoryboard::Finish</a>



<a href="https://msdn.microsoft.com/8ee9a17f-c57c-49df-950d-491e05ba8768">IUIAnimationStoryboard::GetStatus</a>



<a href="https://msdn.microsoft.com/02830092-0070-44dc-8db2-239941134473">UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

