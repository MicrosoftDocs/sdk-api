---
UID: NF:uianimation.IUIAnimationVariable2.GetFinalIntegerValue
title: IUIAnimationVariable2::GetFinalIntegerValue
author: windows-sdk-content
description: Gets the final integer value of the animation variable. This is the value after all currently scheduled animations have completed.
old-location: uianimation\iuianimationvariable2_getfinalintegervalue.htm
old-project: UIAnimation
ms.assetid: 290EC1D8-007D-44A0-B3F8-384A9594FDC4
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetFinalIntegerValue, GetFinalIntegerValue method [Windows Animation], GetFinalIntegerValue method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetFinalIntegerValue method, IUIAnimationVariable2.GetFinalIntegerValue, IUIAnimationVariable2::GetFinalIntegerValue, uianimation.iuianimationvariable2_getfinalintegervalue, uianimation/IUIAnimationVariable2::GetFinalIntegerValue
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
 - IUIAnimationVariable2.GetFinalIntegerValue
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariable2::GetFinalIntegerValue


## -description


Gets the final integer value of the animation variable. This is the value after all currently scheduled animations have completed.


## -parameters




### -param finalValue [out]

The final value of the animation variable as an integer.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/A676EF27-B59D-4D2D-AD5B-8F46EE337E69">IUIAnimationVariable2</a>
 

 

