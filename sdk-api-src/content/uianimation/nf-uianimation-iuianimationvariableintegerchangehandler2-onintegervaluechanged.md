---
UID: NF:uianimation.IUIAnimationVariableIntegerChangeHandler2.OnIntegerValueChanged
title: IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged
author: windows-sdk-content
description: Handles events that occur when the integer value of an animation variable changes in the specified dimension.
old-location: uianimation\iuianimationvariableintegerchangehandler2_onintegervaluechanged.htm
tech.root: UIAnimation
ms.assetid: 76889784-BF1B-475B-8D84-201BEE6F0594
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IUIAnimationVariableIntegerChangeHandler2 interface [Windows Animation],OnIntegerValueChanged method, IUIAnimationVariableIntegerChangeHandler2.OnIntegerValueChanged, IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged, OnIntegerValueChanged, OnIntegerValueChanged method [Windows Animation], OnIntegerValueChanged method [Windows Animation],IUIAnimationVariableIntegerChangeHandler2 interface, uianimation.iuianimationvariableintegerchangehandler2_onintegervaluechanged, uianimation/IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged
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
 - IUIAnimationVariableIntegerChangeHandler2.OnIntegerValueChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uianimation.h
: 
- IUIAnimationVariableIntegerChangeHandler2.OnIntegerValueChanged
: 
---

# IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged


## -description


Handles events that occur when the integer value of an animation variable changes in the specified dimension.


## -parameters




### -param storyboard [in]

The storyboard that is animating the animation variable specified by the <i>variable</i> parameter.


### -param variable [in]

The animation variable that has been updated.


### -param newValue [in]

The new integer value of the animation variable.

<div class="alert"><b>Note</b>  The rounding mode for an animation variable is specified using the <a href="https://msdn.microsoft.com/D2FCC17B-0584-4317-8BD7-25454E4A553C">SetRoundingMode</a> method.</div>
<div> </div>

### -param previousValue [in]

The previous integer value of the animation variable.

<div class="alert"><b>Note</b>  The rounding mode for an animation variable is specified using the <a href="https://msdn.microsoft.com/D2FCC17B-0584-4317-8BD7-25454E4A553C">SetRoundingMode</a> method.</div>
<div> </div>

### -param cDimension [in]

The dimension in which the integer value of the animation variable changed.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method receives updates as <b>INT32</b> values.  
         To receive updates as <b>DOUBLE</b> values, use the <a href="https://msdn.microsoft.com/3C885518-8EAC-4123-83A5-5DEB27523DEF">OnValueChanged</a> method.

<b>OnIntegerValueChanged</b> events might occur less frequently than <a href="https://msdn.microsoft.com/3C885518-8EAC-4123-83A5-5DEB27523DEF">OnValueChanged</a> events because values such as 2.2, 2.3, and 2.4 would all be rounded to the same integer.

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnIntegerValueChanged</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/7925D462-C3FD-4BD2-806D-66FE822979EF">GetValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/FF39BE67-AED7-4B67-ABAF-D5D51619F0D3">GetFinalValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1A2BF7DB-1C7B-43BF-A7F7-A4FB47250597">GetPreviousValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C878B86A-87AD-457A-802A-9A329B401B08">GetIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/290EC1D8-007D-44A0-B3F8-384A9594FDC4">GetFinalIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8B25BE8D-B12F-44B4-AFBF-3E6994BA0771">GetPreviousIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7A9B4A84-94E4-4B6C-B2FF-0A0A70397D21">GetCurrentStoryboard</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ED367DB7-91D6-4D2E-BDAB-27FA4340F091">GetVariableFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C7B11A34-E5FB-40D7-A655-29D28ECF4068">GetStoryboardFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A73D5003-FC28-4A79-B157-3D0D2E0DEB3D">GetTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/29E6CA4D-527D-4C9D-9E28-2E2C67516126">GetTag</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/A8D3B617-43D6-4541-AE98-1332DB5205CE">IUIAnimationVariableChangeHandler2</a>



<a href="https://msdn.microsoft.com/778BE01B-360C-431C-9515-DE43B4F2B77D">IUIAnimationVariableIntegerChangeHandler2</a>



<a href="https://msdn.microsoft.com/3C885518-8EAC-4123-83A5-5DEB27523DEF">OnValueChanged</a>



<a href="https://msdn.microsoft.com/4327AC4A-2C2C-4C1A-AFCD-D2BA8ECEBA12">SetVariableIntegerChangeHandler</a>



<a href="https://msdn.microsoft.com/0221207b-4583-44b8-85aa-dc6cd4cd9d25">UI_ANIMATION_ROUNDING_MODE</a>
 

 

