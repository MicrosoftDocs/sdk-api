---
UID: NF:uianimation.IUIAnimationInterpolator2.GetFinalValue
title: IUIAnimationInterpolator2::GetFinalValue
author: windows-sdk-content
description: Gets the final value at the end of the transition for the given dimension.
old-location: uianimation\iuianimationinterpolator2_getfinalvalue.htm
old-project: UIAnimation
ms.assetid: 330816C7-1641-41FA-8FB9-56FCE0108593
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetFinalValue, GetFinalValue method [Windows Animation], GetFinalValue method [Windows Animation],IUIAnimationInterpolator2 interface, IUIAnimationInterpolator2 interface [Windows Animation],GetFinalValue method, IUIAnimationInterpolator2.GetFinalValue, IUIAnimationInterpolator2::GetFinalValue, uianimation.iuianimationinterpolator2_getfinalvalue, uianimation/IUIAnimationInterpolator2::GetFinalValue
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
tech.root: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationInterpolator2.GetFinalValue
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationInterpolator2::GetFinalValue


## -description


Gets the final value at the end of the transition for the given dimension.


## -parameters




### -param value [out]

The final value.


### -param cDimension [in]

The dimension from which to retrieve the final value.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Windows Animation always calls the <a href="https://msdn.microsoft.com/F1C0C54D-86C3-4B65-96A4-66D89F2B2084">IUIAnimationInterpolator2::SetInitialValueAndVelocity</a> method to set the initial value and velocity before calling <b>GetFinalValue</b>, so a custom interpolator need not check whether the initial value and velocity have been set.

Windows Animation can call <a href="https://msdn.microsoft.com/F1C0C54D-86C3-4B65-96A4-66D89F2B2084">SetInitialValueAndVelocity</a> multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to <b>GetFinalValue</b> reflect the updated state.




## -see-also




<a href="https://msdn.microsoft.com/EC0D1933-37C3-41E2-AB13-DA4AAF4B8F04">IUIAnimationInterpolator2</a>
 

 

