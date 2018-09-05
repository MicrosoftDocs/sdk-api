---
UID: NF:uianimation.IUIAnimationInterpolator.SetInitialValueAndVelocity
title: IUIAnimationInterpolator::SetInitialValueAndVelocity
author: windows-sdk-content
description: Sets the initial value and velocity at the start of the transition.
old-location: uianimation\iuianimationinterpolator_setinitialvalueandvelocity.htm
old-project: UIAnimation
ms.assetid: a1c5451a-b8d0-4eb7-883c-6bd1d585cb11
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUIAnimationInterpolator interface [Windows Animation],SetInitialValueAndVelocity method, IUIAnimationInterpolator.SetInitialValueAndVelocity, IUIAnimationInterpolator::SetInitialValueAndVelocity, SetInitialValueAndVelocity, SetInitialValueAndVelocity method [Windows Animation], SetInitialValueAndVelocity method [Windows Animation],IUIAnimationInterpolator interface, uianimation.iuianimationinterpolator_setinitialvalueandvelocity, uianimation/IUIAnimationInterpolator::SetInitialValueAndVelocity
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
 - IUIAnimationInterpolator.SetInitialValueAndVelocity
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationInterpolator::SetInitialValueAndVelocity


## -description


Sets the initial value and velocity at the start of the transition.


## -parameters




### -param initialValue [in]

The initial value.


### -param initialVelocity [in]

The initial velocity.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. 
            
          See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Windows Animation always calls <b>SetInitialValueAndVelocity</b> before calling the other methods of  <a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a> at different offsets. However, it can be called multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to these methods reflect the updated state.




## -see-also




<a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a>
 

 

