---
UID: NF:uianimation.IUIAnimationManager.SetAnimationMode
title: IUIAnimationManager::SetAnimationMode
author: windows-sdk-content
description: Sets the animation mode.
old-location: uianimation\iuianimationmanager_setanimationmode.htm
old-project: UIAnimation
ms.assetid: b5d6c5f1-1e1c-497f-a556-f419e2c68585
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],SetAnimationMode method, IUIAnimationManager.SetAnimationMode, IUIAnimationManager::SetAnimationMode, SetAnimationMode, SetAnimationMode method [Windows Animation], SetAnimationMode method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_setanimationmode, uianimation/IUIAnimationManager::SetAnimationMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationManager.SetAnimationMode
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager::SetAnimationMode


## -description


Sets the animation mode.


## -parameters




### -param mode [in]

The animation mode.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method is used to enable or disable animation globally. While animation is disabled, all storyboards finish immediately when they are scheduled. The default mode is <b>UI_ANIMATION_MODE_SYSTEM_DEFAULT</b>, which lets Windows decide when to enable or disable animation in the application.




## -see-also




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>



<a href="https://msdn.microsoft.com/b8995687-c0dc-4cd7-b11a-f871172895f9">UI_ANIMATION_MODE</a>
 

 

