---
UID: NF:uianimation.IUIAnimationVariable2.SetLowerBoundVector
title: IUIAnimationVariable2::SetLowerBoundVector
author: windows-sdk-content
description: Sets the lower bound (floor) value of each specified dimension for the animation variable. The value of each animation variable should not fall below its lower bound.
old-location: uianimation\iuianimationvariable2_setlowerboundvector.htm
old-project: UIAnimation
ms.assetid: CB7D30BF-D22C-40EB-A530-035CED1BDAF0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IUIAnimationVariable2 interface [Windows Animation],SetLowerBoundVector method, IUIAnimationVariable2.SetLowerBoundVector, IUIAnimationVariable2::SetLowerBoundVector, SetLowerBoundVector, SetLowerBoundVector method [Windows Animation], SetLowerBoundVector method [Windows Animation],IUIAnimationVariable2 interface, uianimation.iuianimationvariable2_setlowerboundvector, uianimation/IUIAnimationVariable2::SetLowerBoundVector
ms.prod: windows
ms.technology: windows-sdk
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
 - IUIAnimationVariable2.SetLowerBoundVector
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariable2::SetLowerBoundVector


## -description


Sets the lower bound (floor) value of each specified dimension for the animation variable. The value of each animation variable should not fall below its lower bound.


## -parameters




### -param bound [in]

A vector (of size <i>cDimension</i>) that contains  the lower bound values of each dimension.


### -param cDimension [in]

The number of dimensions that require lower bound values. This parameter specifies the number of values listed in <i>bound</i>.


## -returns



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/A676EF27-B59D-4D2D-AD5B-8F46EE337E69">IUIAnimationVariable2</a>
 

 

