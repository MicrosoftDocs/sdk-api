---
UID: NF:uianimation.IUIAnimationStoryboard.Finish
title: IUIAnimationStoryboard::Finish (uianimation.h)
author: windows-sdk-content
description: Finishes the storyboard within the specified time, compressing the storyboard if necessary.
old-location: uianimation\iuianimationstoryboard_finish.htm
tech.root: UIAnimation
ms.assetid: 45d0872a-dbcf-4151-a880-80b2c6fb884c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Finish, Finish method [Windows Animation], Finish method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],Finish method, IUIAnimationStoryboard.Finish, IUIAnimationStoryboard::Finish, uianimation.iuianimationstoryboard_finish, uianimation/IUIAnimationStoryboard::Finish
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
 - IUIAnimationStoryboard.Finish
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationStoryboard::Finish


## -description


Finishes the storyboard within the specified time, compressing the storyboard if necessary.


## -parameters




### -param completionDeadline [in]

The maximum amount of time that the storyboard can use to finish playing.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method has no effect on storyboard events. Events continue to be raised as expected while the storyboard plays.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-finishallstoryboards">IUIAnimationManager::FinishAllStoryboards</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-abandon">IUIAnimationStoryboard::Abandon</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-conclude">IUIAnimationStoryboard::Conclude</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-schedule">IUIAnimationStoryboard::Schedule</a>
 

 

