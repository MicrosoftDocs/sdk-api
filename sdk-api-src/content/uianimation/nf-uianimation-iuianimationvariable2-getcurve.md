---
UID: NF:uianimation.IUIAnimationVariable2.GetCurve
title: IUIAnimationVariable2::GetCurve (uianimation.h)
author: windows-sdk-content
description: Gets the animation curve of the animation variable.
old-location: uianimation\iuianimationvariable2_getcurve.htm
tech.root: UIAnimation
ms.assetid: 59E7C7A1-2461-487C-A263-A9DFC851B720
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCurve, GetCurve method [Windows Animation], GetCurve method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetCurve method, IUIAnimationVariable2.GetCurve, IUIAnimationVariable2::GetCurve, uianimation.iuianimationvariable2_getcurve, uianimation/IUIAnimationVariable2::GetCurve
ms.topic: method
f1_keywords: 
 - "uianimation/IUIAnimationVariable2.GetCurve"
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
 - IUIAnimationVariable2.GetCurve
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationVariable2::GetCurve


## -description


Gets the animation curve of the animation variable.


## -parameters




### -param animation [in]

The object that generates a sequence of animation curve primitives.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



The application implements the <a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a> object that is referenced by the <i>animation</i> parameter.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>
 

 

