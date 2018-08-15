---
UID: NF:uianimation.IUIAnimationVariable2.SetRoundingMode
title: IUIAnimationVariable2::SetRoundingMode
author: windows-sdk-content
description: Sets the rounding mode of the animation variable.
old-location: uianimation\iuianimationvariable2_setroundingmode.htm
old-project: UIAnimation
ms.assetid: D2FCC17B-0584-4317-8BD7-25454E4A553C
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUIAnimationVariable2 interface [Windows Animation],SetRoundingMode method, IUIAnimationVariable2.SetRoundingMode, IUIAnimationVariable2::SetRoundingMode, SetRoundingMode, SetRoundingMode method [Windows Animation], SetRoundingMode method [Windows Animation],IUIAnimationVariable2 interface, uianimation.iuianimationvariable2_setroundingmode, uianimation/IUIAnimationVariable2::SetRoundingMode
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
 - IUIAnimationVariable2.SetRoundingMode
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariable2::SetRoundingMode


## -description


Sets the rounding mode of the animation variable.


## -parameters




### -param mode [in]

The rounding mode.


## -returns



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



An animation variable's rounding mode determines how a floating-point value is converted to an integer.
      The default mode for each variable is <b>UI_ANIMATION_ROUNDING_NEAREST</b>.




## -see-also




<a href="https://msdn.microsoft.com/A676EF27-B59D-4D2D-AD5B-8F46EE337E69">IUIAnimationVariable2</a>



<a href="https://msdn.microsoft.com/290EC1D8-007D-44A0-B3F8-384A9594FDC4">IUIAnimationVariable2::GetFinalIntegerValue</a>



<a href="https://msdn.microsoft.com/C878B86A-87AD-457A-802A-9A329B401B08">IUIAnimationVariable2::GetIntegerValue</a>



<a href="https://msdn.microsoft.com/8B25BE8D-B12F-44B4-AFBF-3E6994BA0771">IUIAnimationVariable2::GetPreviousIntegerValue</a>



<a href="https://msdn.microsoft.com/0221207b-4583-44b8-85aa-dc6cd4cd9d25">UI_ANIMATION_ROUNDING_MODE</a>
 

 

