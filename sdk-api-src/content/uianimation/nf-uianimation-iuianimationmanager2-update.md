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



Calling this method advances the animation manager to <i>timeNow</i>, changes the status of all storyboards as necessary, and updates any animation variables to appropriate interpolated values. If the animation manager is paused, no storyboards or variables are updated. If the animation  mode is <a href="https://msdn.microsoft.com/b8995687-c0dc-4cd7-b11a-f871172895f9">UI_ANIMATION_MODE_DISABLED</a>, all scheduled storyboards finish playing immediately. If the values of any variables change during this call, the value of <i>updateResult</i> is <a href="https://msdn.microsoft.com/19b1d80f-39b3-4046-aa6a-5312e004b4b0">UI_ANIMATION_UPDATE_VARIABLES_CHANGED</a>; otherwise, it is <a href="https://msdn.microsoft.com/19b1d80f-39b3-4046-aa6a-5312e004b4b0">UI_ANIMATION_UPDATE_NO_CHANGE</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">IUIAnimationManager2</a>



<a href="https://msdn.microsoft.com/AA8EEFD5-A386-4DF1-BCBE-12A92D235E98">IUIAnimationManager2::Pause</a>



<a href="https://msdn.microsoft.com/943BCFBB-3E16-4CC8-BA9F-06D4C99B1DF0">IUIAnimationManager2::Resume</a>



<a href="https://msdn.microsoft.com/BA568B62-7A85-4758-BB04-B4AF617A8443">
      IUIAnimationManager::SetAnimationMode</a>



<a href="https://msdn.microsoft.com/b8995687-c0dc-4cd7-b11a-f871172895f9">
      UI_ANIMATION_MODE</a>



<a href="https://msdn.microsoft.com/19b1d80f-39b3-4046-aa6a-5312e004b4b0">
      UI_ANIMATION_UPDATE_RESULT</a>
 

 

