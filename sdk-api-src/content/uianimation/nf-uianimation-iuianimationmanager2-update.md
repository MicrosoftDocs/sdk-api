---
UID: NF:uianimation.IUIAnimationManager2.Update
title: IUIAnimationManager2::Update (uianimation.h)
author: windows-sdk-content
description: Updates the values of all animation variables.
old-location: uianimation\iuianimationmanager2_update.htm
tech.root: UIAnimation
ms.assetid: 5735ABDB-E1AE-41C0-9F37-92084CEF6FAD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],Update method, IUIAnimationManager2.Update, IUIAnimationManager2::Update, Update, Update method [Windows Animation], Update method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_update, uianimation/IUIAnimationManager2::Update
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
 - IUIAnimationManager2.Update
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationManager2::Update


## -description


Updates the values of all animation variables.


## -parameters




### -param timeNow [in]

The current system time. This parameter must be greater than or equal to 0.0.


### -param updateResult [out, optional]

The result of the update.
            You can omit this parameter from calls to this method.


## -returns



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Calling this method advances the animation manager to <i>timeNow</i>, changes the status of all storyboards as necessary, and updates any animation variables to appropriate interpolated values. If the animation manager is paused, no storyboards or variables are updated. If the animation  mode is <a href="https://msdn.microsoft.com/en-us/library/Dd317046(v=VS.85).aspx">UI_ANIMATION_MODE_DISABLED</a>, all scheduled storyboards finish playing immediately. If the values of any variables change during this call, the value of <i>updateResult</i> is <a href="https://msdn.microsoft.com/en-us/library/Dd371974(v=VS.85).aspx">UI_ANIMATION_UPDATE_VARIABLES_CHANGED</a>; otherwise, it is <a href="https://msdn.microsoft.com/en-us/library/Dd371974(v=VS.85).aspx">UI_ANIMATION_UPDATE_NO_CHANGE</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">IUIAnimationManager2</a>



<a href="https://msdn.microsoft.com/AA8EEFD5-A386-4DF1-BCBE-12A92D235E98">IUIAnimationManager2::Pause</a>



<a href="https://msdn.microsoft.com/943BCFBB-3E16-4CC8-BA9F-06D4C99B1DF0">IUIAnimationManager2::Resume</a>



<a href="https://msdn.microsoft.com/BA568B62-7A85-4758-BB04-B4AF617A8443">IUIAnimationManager::SetAnimationMode</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd317046(v=VS.85).aspx">UI_ANIMATION_MODE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371974(v=VS.85).aspx">UI_ANIMATION_UPDATE_RESULT</a>
 

 

