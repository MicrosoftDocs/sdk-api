---
UID: NF:uianimation.IUIAnimationVariable2.GetCurve
title: IUIAnimationVariable2::GetCurve
author: windows-sdk-content
description: Gets the animation curve of the animation variable.
old-location: uianimation\iuianimationvariable2_getcurve.htm
tech.root: UIAnimation
ms.assetid: 59E7C7A1-2461-487C-A263-A9DFC851B720
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetCurve, GetCurve method [Windows Animation], GetCurve method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetCurve method, IUIAnimationVariable2.GetCurve, IUIAnimationVariable2::GetCurve, uianimation.iuianimationvariable2_getcurve, uianimation/IUIAnimationVariable2::GetCurve
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IUIAnimationVariable2.GetCurve
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationVariable2::GetCurve


## -description


Gets the animation curve of the animation variable.


## -parameters




### -param animation [in]

The object that generates a sequence of animation curve primitives.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



The application implements the <a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a> object that is referenced by the <i>animation</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/A676EF27-B59D-4D2D-AD5B-8F46EE337E69">IUIAnimationVariable2</a>
 

 

