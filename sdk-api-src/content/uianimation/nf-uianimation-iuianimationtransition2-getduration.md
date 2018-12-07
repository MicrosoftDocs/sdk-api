---
UID: NF:uianimation.IUIAnimationTransition2.GetDuration
title: IUIAnimationTransition2::GetDuration
author: windows-sdk-content
description: Gets the duration of the transition.
old-location: uianimation\iuianimationtransition2_getduration.htm
tech.root: UIAnimation
ms.assetid: 07B5C7D7-80B1-4458-93A7-39F61121B618
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDuration, GetDuration method [Windows Animation], GetDuration method [Windows Animation],IUIAnimationTransition2 interface, IUIAnimationTransition2 interface [Windows Animation],GetDuration method, IUIAnimationTransition2.GetDuration, IUIAnimationTransition2::GetDuration, uianimation.iuianimationtransition2_getduration, uianimation/IUIAnimationTransition2::GetDuration
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
 - IUIAnimationTransition2.GetDuration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationTransition2::GetDuration


## -description


Gets the duration of the transition.


## -parameters




### -param duration [out]

The duration of the transition, in seconds.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



An application should typically call the <a href="https://msdn.microsoft.com/A73065A7-B191-4CB9-A75A-827CFC040C92">IsDurationKnown</a> method before calling this method. 

This method should not be called when the storyboard to which the transition has been added is scheduled or playing.




## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>
 

 

