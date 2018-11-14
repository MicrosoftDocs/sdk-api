---
UID: NF:uianimation.IUIAnimationInterpolator.GetFinalValue
title: IUIAnimationInterpolator::GetFinalValue
author: windows-sdk-content
description: Gets the final value at the end of the transition.
old-location: uianimation\iuianimationinterpolator_getfinalvalue.htm
tech.root: UIAnimation
ms.assetid: 5f99fc36-1f56-4275-9b6f-c22bde929d22
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetFinalValue, GetFinalValue method [Windows Animation], GetFinalValue method [Windows Animation],IUIAnimationInterpolator interface, IUIAnimationInterpolator interface [Windows Animation],GetFinalValue method, IUIAnimationInterpolator.GetFinalValue, IUIAnimationInterpolator::GetFinalValue, uianimation.iuianimationinterpolator_getfinalvalue, uianimation/IUIAnimationInterpolator::GetFinalValue
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
 - IUIAnimationInterpolator.GetFinalValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uianimation.h
: 
- IUIAnimationInterpolator.GetFinalValue
: 
---

# IUIAnimationInterpolator::GetFinalValue


## -description


Gets the final value at the end of the transition.


## -parameters




### -param value [out]

The final value.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. 
          See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Windows Animation always calls the <a href="https://msdn.microsoft.com/a1c5451a-b8d0-4eb7-883c-6bd1d585cb11">SetInitialValueAndVelocity</a> method to set the initial value and velocity before calling <b>GetFinalValue</b>, so a custom interpolator need not check whether the initial value and velocity have been set.

Windows Animation can call <a href="https://msdn.microsoft.com/a1c5451a-b8d0-4eb7-883c-6bd1d585cb11">SetInitialValueAndVelocity</a> multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to <b>GetFinalValue</b> reflect the updated state.




## -see-also




<a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a>
 

 

