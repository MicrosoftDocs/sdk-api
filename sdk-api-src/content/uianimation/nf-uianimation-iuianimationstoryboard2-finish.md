---
UID: NF:uianimation.IUIAnimationStoryboard2.Finish
title: IUIAnimationStoryboard2::Finish
author: windows-sdk-content
description: Finishes the storyboard within the specified time, compressing the storyboard if necessary.
old-location: uianimation\iuianimationstoryboard2_finish.htm
tech.root: UIAnimation
ms.assetid: 632BC77D-F2C5-4D08-8E9C-0598617A1DA7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Finish, Finish method [Windows Animation], Finish method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],Finish method, IUIAnimationStoryboard2.Finish, IUIAnimationStoryboard2::Finish, uianimation.iuianimationstoryboard2_finish, uianimation/IUIAnimationStoryboard2::Finish
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps \| UWP apps]
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
 - IUIAnimationStoryboard2.Finish
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboard2::Finish


## -description


Finishes the storyboard within the specified time, compressing the storyboard if necessary.


## -parameters




### -param completionDeadline

The maximum amount of time that the storyboard can use to finish playing.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method has no effect on storyboard events. Events continue to be raised as expected while the storyboard plays.




## -see-also




<a href="https://msdn.microsoft.com/830A5D30-68FF-4226-AC7C-7B1C5F7BA367">IUIAnimationManager2::FinishAllStoryboards</a>



<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/ABB7184F-A703-45E3-96D8-E3062EEB9565">IUIAnimationStoryboard2::Abandon</a>



<a href="https://msdn.microsoft.com/C7687E52-433F-4E73-910D-86298E528F7B">IUIAnimationStoryboard2::Conclude</a>



<a href="https://msdn.microsoft.com/9F20AE4A-F693-4DDA-90F4-FCCA5291208B">IUIAnimationStoryboard2::Schedule</a>
 

 

