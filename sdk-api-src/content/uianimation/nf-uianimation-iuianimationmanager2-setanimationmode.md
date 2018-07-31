---
UID: NF:uianimation.IUIAnimationManager2.SetAnimationMode
title: IUIAnimationManager2::SetAnimationMode
author: windows-sdk-content
description: Sets the animation mode.
old-location: uianimation\iuianimationmanager2_setanimationmode.htm
old-project: UIAnimation
ms.assetid: BA568B62-7A85-4758-BB04-B4AF617A8443
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],SetAnimationMode method, IUIAnimationManager2.SetAnimationMode, IUIAnimationManager2::SetAnimationMode, SetAnimationMode, SetAnimationMode method [Windows Animation], SetAnimationMode method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_setanimationmode, uianimation/IUIAnimationManager2::SetAnimationMode
ms.prod: windows
ms.technology: windows-sdk
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
 - IUIAnimationManager2.SetAnimationMode
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager2::SetAnimationMode


## -description


Sets the animation mode.


## -parameters




### -param mode [in]

The animation mode.


## -returns



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Use this method to enable or disable animation globally. While animation is disabled, all storyboards finish immediately when they are scheduled. The default mode is <a href="https://msdn.microsoft.com/b8995687-c0dc-4cd7-b11a-f871172895f9">UI_ANIMATION_MODE_SYSTEM_DEFAULT</a>, which lets Windows decide when to enable or disable animation in the application.




## -see-also




<a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">IUIAnimationManager2</a>



<a href="https://msdn.microsoft.com/b8995687-c0dc-4cd7-b11a-f871172895f9">UI_ANIMATION_MODE</a>
 

 

