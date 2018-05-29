---
UID: NF:uianimation.IUIAnimationVariable2.GetPreviousVectorValue
title: IUIAnimationVariable2::GetPreviousVectorValue
author: windows-sdk-content
description: Gets the previous value of the animation variable for the specified dimension. This is the value of the animation variable before the most recent update.
old-location: uianimation\iuianimationvariable2_getpreviousvectorvalue.htm
old-project: UIAnimation
ms.assetid: E6C32B28-A6DE-47FB-8399-CA0B782D8B25
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetPreviousVectorValue, GetPreviousVectorValue method [Windows Animation], GetPreviousVectorValue method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetPreviousVectorValue method, IUIAnimationVariable2.GetPreviousVectorValue, IUIAnimationVariable2::GetPreviousVectorValue, uianimation.iuianimationvariable2_getpreviousvectorvalue, uianimation/IUIAnimationVariable2::GetPreviousVectorValue
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
-	IUIAnimationVariable2.GetPreviousVectorValue
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariable2::GetPreviousVectorValue


## -description


Gets the previous value of the animation variable for the specified dimension. This is the value of the animation variable before the most recent update.


## -parameters




### -param previousValue [out]

The previous value of the animation variable.


### -param cDimension [in]

The dimension from which to get the value of the animation variable.



## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/A676EF27-B59D-4D2D-AD5B-8F46EE337E69">IUIAnimationVariable2</a>
 

 

