---
UID: NF:uianimation.IUIAnimationInterpolator2.GetPrimitiveInterpolation
title: IUIAnimationInterpolator2::GetPrimitiveInterpolation (uianimation.h)
author: windows-sdk-content
description: Generates a primitive interpolation of the specified animation curve.
old-location: uianimation\iuianimationinterpolator2_getprimitiveinterpolation.htm
tech.root: UIAnimation
ms.assetid: E3CE4D97-08C8-46F4-B8B0-42CA4212DF50
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPrimitiveInterpolation, GetPrimitiveInterpolation method [Windows Animation], GetPrimitiveInterpolation method [Windows Animation],IUIAnimationInterpolator2 interface, IUIAnimationInterpolator2 interface [Windows Animation],GetPrimitiveInterpolation method, IUIAnimationInterpolator2.GetPrimitiveInterpolation, IUIAnimationInterpolator2::GetPrimitiveInterpolation, uianimation.iuianimationinterpolator2_getprimitiveinterpolation, uianimation/IUIAnimationInterpolator2::GetPrimitiveInterpolation
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
 - IUIAnimationInterpolator2.GetPrimitiveInterpolation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationInterpolator2::GetPrimitiveInterpolation


## -description


Generates a primitive interpolation of the specified animation curve.


## -parameters




### -param interpolation [in]

The object that defines the custom animation curve information.


### -param cDimension [in]

The dimension in which to apply the new segment.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/EC0D1933-37C3-41E2-AB13-DA4AAF4B8F04">IUIAnimationInterpolator2</a>



<a href="https://msdn.microsoft.com/6EAE7874-1103-4D2E-A325-37E5A95705F5">IUIAnimationPrimitiveInterpolation</a>
 

 

