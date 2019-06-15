---
UID: NF:uianimation.IUIAnimationTransition2.SetInitialVectorValue
title: IUIAnimationTransition2::SetInitialVectorValue (uianimation.h)
author: windows-sdk-content
description: Sets the initial value of the transition for each specified dimension in the animation variable.
old-location: uianimation\iuianimationtransition2_setinitialvectorvalue.htm
tech.root: UIAnimation
ms.assetid: B46F15F2-8C2A-4F15-9BBE-20FB8E5C84C6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransition2 interface [Windows Animation],SetInitialVectorValue method, IUIAnimationTransition2.SetInitialVectorValue, IUIAnimationTransition2::SetInitialVectorValue, SetInitialVectorValue, SetInitialVectorValue method [Windows Animation], SetInitialVectorValue method [Windows Animation],IUIAnimationTransition2 interface, uianimation.iuianimationtransition2_setinitialvectorvalue, uianimation/IUIAnimationTransition2::SetInitialVectorValue
ms.topic: method
f1_keywords: ["uianimation/IUIAnimationTransition2.SetInitialVectorValue"]
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
 - IUIAnimationTransition2.SetInitialVectorValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationTransition2::SetInitialVectorValue


## -description


Sets the initial value of the transition for each specified dimension in the animation variable.


## -parameters




### -param value [in]

A vector (of size <i>cDimension</i>) that contains  the initial values for the transition.


### -param cDimension [in]

The number of dimensions that require transition values. This parameter specifies the number of values listed in <i>value</i>.


## -returns



Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



The animation manager should not call this method after the transition has been added to a storyboard.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>
 

 

