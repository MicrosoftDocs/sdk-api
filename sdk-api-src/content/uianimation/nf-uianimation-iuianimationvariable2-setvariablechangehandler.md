---
UID: NF:uianimation.IUIAnimationVariable2.SetVariableChangeHandler
title: IUIAnimationVariable2::SetVariableChangeHandler
author: windows-sdk-content
description: Specifies a handler for changes to the value of the animation variable.
old-location: uianimation\iuianimationvariable2_setvariablechangehandler.htm
tech.root: UIAnimation
ms.assetid: F603C693-8F91-483F-8B0A-712E03BC10E5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAnimationVariable2 interface [Windows Animation],SetVariableChangeHandler method, IUIAnimationVariable2.SetVariableChangeHandler, IUIAnimationVariable2::SetVariableChangeHandler, SetVariableChangeHandler, SetVariableChangeHandler method [Windows Animation], SetVariableChangeHandler method [Windows Animation],IUIAnimationVariable2 interface, uianimation.iuianimationvariable2_setvariablechangehandler, uianimation/IUIAnimationVariable2::SetVariableChangeHandler
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
 - IUIAnimationVariable2.SetVariableChangeHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationVariable2::SetVariableChangeHandler


## -description


Specifies a handler for changes to the value of the animation variable. 


## -parameters




### -param handler [in, optional]

The handler for changes to the value of the animation variable. This parameter can be <b>NULL</b>.




### -param fRegisterForNextAnimationEvent [in]

If <b>TRUE</b>, specifies that the <a href="https://msdn.microsoft.com/C2F049B7-287F-4EC2-A737-965E01515056">EstimateNextEventTime</a> method will incorporate <i>handler</i> into its estimate of the time interval until the next animation event. No default value.


## -returns



Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Passing <b>NULL</b> for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object that you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="https://msdn.microsoft.com/F66A987C-E020-4CD6-BE3F-440C3F8B8CF2">IUIAnimationManager2::Shutdown</a> method.




## -see-also




<a href="https://msdn.microsoft.com/A676EF27-B59D-4D2D-AD5B-8F46EE337E69">IUIAnimationVariable2</a>



<a href="https://msdn.microsoft.com/4327AC4A-2C2C-4C1A-AFCD-D2BA8ECEBA12">IUIAnimationVariable2::SetVariableIntegerChangeHandler</a>



<a href="https://msdn.microsoft.com/A8D3B617-43D6-4541-AE98-1332DB5205CE">IUIAnimationVariableChangeHandler2</a>
 

 

