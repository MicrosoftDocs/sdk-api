---
UID: NF:uianimation.IUIAnimationTransition2.SetInitialValue
title: IUIAnimationTransition2::SetInitialValue
author: windows-sdk-content
description: Sets the initial value of the transition.
old-location: uianimation\iuianimationtransition2_setinitialvalue.htm
old-project: UIAnimation
ms.assetid: 813224BE-369D-4D65-AA12-AEE590627F40
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUIAnimationTransition2 interface [Windows Animation],SetInitialValue method, IUIAnimationTransition2.SetInitialValue, IUIAnimationTransition2::SetInitialValue, SetInitialValue, SetInitialValue method [Windows Animation], SetInitialValue method [Windows Animation],IUIAnimationTransition2 interface, uianimation.iuianimationtransition2_setinitialvalue, uianimation/IUIAnimationTransition2::SetInitialValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.redist: 
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
 - IUIAnimationTransition2.SetInitialValue
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransition2::SetInitialValue


## -description


Sets the initial value of the transition.


## -parameters




### -param value [in]

The initial value for the transition.


## -returns



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Do not call this method after the transition has been added to a storyboard.




## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>
 

 

