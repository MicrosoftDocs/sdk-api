---
UID: NF:uianimation.IUIAnimationTransition2.IsDurationKnown
title: IUIAnimationTransition2::IsDurationKnown
author: windows-sdk-content
description: Determines whether the duration of a transition is known.
old-location: uianimation\iuianimationtransition2_isdurationknown.htm
old-project: UIAnimation
ms.assetid: A73065A7-B191-4CB9-A75A-827CFC040C92
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationTransition2 interface [Windows Animation],IsDurationKnown method, IUIAnimationTransition2.IsDurationKnown, IUIAnimationTransition2::IsDurationKnown, IsDurationKnown, IsDurationKnown method [Windows Animation], IsDurationKnown method [Windows Animation],IUIAnimationTransition2 interface, uianimation.iuianimationtransition2_isdurationknown, uianimation/IUIAnimationTransition2::IsDurationKnown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps | UWP apps]
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationTransition2.IsDurationKnown
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransition2::IsDurationKnown


## -description


Determines whether the duration of a transition is known.


## -parameters






## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method should not be called when the storyboard to which the transition has been added is scheduled or playing.




## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/07B5C7D7-80B1-4458-93A7-39F61121B618">IUIAnimationTransition2::GetDuration</a>
 

 

