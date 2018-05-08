---
UID: NF:uianimation.IUIAnimationVariable2.GetFinalIntegerVectorValue
title: IUIAnimationVariable2::GetFinalIntegerVectorValue
author: windows-driver-content
description: Gets the final integer value of the animation variable for the specified dimension. This is the value after all currently scheduled animations have completed.
old-location: uianimation\iuianimationvariable2_getfinalintegervectorvalue.htm
old-project: UIAnimation
ms.assetid: 191DA982-E3F1-4E37-A4D8-7813201E6B6B
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetFinalIntegerVectorValue, GetFinalIntegerVectorValue method [Windows Animation], GetFinalIntegerVectorValue method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetFinalIntegerVectorValue method, IUIAnimationVariable2.GetFinalIntegerVectorValue, IUIAnimationVariable2::GetFinalIntegerVectorValue, uianimation.iuianimationvariable2_getfinalintegervectorvalue, uianimation/IUIAnimationVariable2::GetFinalIntegerVectorValue
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IUIAnimationVariable2.GetFinalIntegerVectorValue
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariable2::GetFinalIntegerVectorValue


## -description


Gets the final integer value of the animation variable for the specified dimension. This is the value after all currently scheduled animations have completed.


## -parameters




### -param finalValue [out]

The final value of the animation variable as an integer.


### -param cDimension [in]

The dimension from which to get the value of the animation variable.



## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/A676EF27-B59D-4D2D-AD5B-8F46EE337E69">IUIAnimationVariable2</a>
 

 

