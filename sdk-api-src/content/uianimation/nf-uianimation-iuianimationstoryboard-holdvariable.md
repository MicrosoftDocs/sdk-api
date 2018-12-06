---
UID: NF:uianimation.IUIAnimationStoryboard.HoldVariable
title: IUIAnimationStoryboard::HoldVariable
author: windows-sdk-content
description: Directs the storyboard to hold the specified animation variable at its final value until the storyboard ends.
old-location: uianimation\iuianimationstoryboard_holdvariable.htm
tech.root: UIAnimation
ms.assetid: ac5ee9c0-cecb-41f1-b8d3-6f779dfafef7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: HoldVariable, HoldVariable method [Windows Animation], HoldVariable method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],HoldVariable method, IUIAnimationStoryboard.HoldVariable, IUIAnimationStoryboard::HoldVariable, uianimation.iuianimationstoryboard_holdvariable, uianimation/IUIAnimationStoryboard::HoldVariable
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
 - IUIAnimationStoryboard.HoldVariable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboard::HoldVariable


## -description


Directs the storyboard to hold the specified animation variable at its final value until the storyboard ends.


## -parameters




### -param variable [in]

The animation variable.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



When a storyboard is playing, it has exclusive access to any variables it animates unless the storyboard is trimmed by a higher priority storyboard. Typically, this exclusive access is released  when the last transition in the storyboard for that variable finishes playing. Applications can call this method to maintain exclusive access to the animation variable and hold the variable, at the final value of the last transition, until the end of the storyboard.




## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>
 

 

