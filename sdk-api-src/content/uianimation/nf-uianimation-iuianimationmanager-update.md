---
UID: NF:uianimation.IUIAnimationManager.Update
title: IUIAnimationManager::Update (uianimation.h)
author: windows-sdk-content
description: Updates the values of all animation variables.
old-location: uianimation\iuianimationmanager_update.htm
tech.root: UIAnimation
ms.assetid: 6008fe44-8d86-4a56-a1e2-7bc144b224b2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],Update method, IUIAnimationManager.Update, IUIAnimationManager::Update, Update, Update method [Windows Animation], Update method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_update, uianimation/IUIAnimationManager::Update
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
 - IUIAnimationManager.Update
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationManager::Update


## -description


Updates the values of all animation variables.


## -parameters




### -param timeNow [in]

The current system time. This parameter must be greater than or equal to 0.0.


### -param updateResult [out, optional]

The result of the update.
            This parameter can be omitted from calls to this method.


## -returns



            
            If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.
            See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Calling this method advances the animation manager to <i>timeNow</i>, changing statuses of storyboards as necessary and updating any animation variables to appropriate interpolated values. If the animation manager is paused, no storyboards or variables are updated. If the animation  mode is <b>UI_ANIMATION_MODE_DISABLED</b>, all scheduled storyboards finish playing immediately. If the values of any variables change during this call, the value of <i>updateResult</i> is <b>UI_ANIMATION_UPDATE_VARIABLES_CHANGED</b>; otherwise, it is <b>UI_ANIMATION_UPDATE_NO_CHANGE</b>.
      


#### Examples

The following example updates the animation manager with the current time. For additional examples, see <a href="https://msdn.microsoft.com/c4f746c3-e47c-4b82-a41b-e2c0d177d097">Update the Animation Manager and Draw Frames</a>.


```cpp
// Update the animation manager with the current time
UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );
if (SUCCEEDED(hr))
{
    UI_ANIMATION_UPDATE_RESULT updateResult;
    hr = m_pAnimationManager->Update(
        secondsNow,
        &updateResult
        );
    if (SUCCEEDED(hr))
    {
        if (updateResult == UI_ANIMATION_UPDATE_VARIABLES_CHANGED)
        {
            ...
        }
    }
}
```





## -see-also




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>



<a href="https://msdn.microsoft.com/52b11e79-9930-4fd8-84b4-152917090519">IUIAnimationManager::Pause</a>



<a href="https://msdn.microsoft.com/f29a9337-0ed0-46f8-ab77-8f82ab39d8df">IUIAnimationManager::Resume</a>



<a href="https://msdn.microsoft.com/b5d6c5f1-1e1c-497f-a556-f419e2c68585">IUIAnimationManager::SetAnimationMode</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd317046(v=VS.85).aspx">UI_ANIMATION_MODE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371974(v=VS.85).aspx">UI_ANIMATION_UPDATE_RESULT</a>
 

 

