---
UID: NF:uianimation.IUIAnimationVariableChangeHandler2.OnValueChanged
title: IUIAnimationVariableChangeHandler2::OnValueChanged
author: windows-sdk-content
description: Handles events that occur when the value of an animation variable changes in the specified dimension.
old-location: uianimation\iuianimationvariablechangehandler2_onvaluechanged.htm
tech.root: UIAnimation
ms.assetid: 3C885518-8EAC-4123-83A5-5DEB27523DEF
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUIAnimationVariableChangeHandler2 interface [Windows Animation],OnValueChanged method, IUIAnimationVariableChangeHandler2.OnValueChanged, IUIAnimationVariableChangeHandler2::OnValueChanged, OnValueChanged, OnValueChanged method [Windows Animation], OnValueChanged method [Windows Animation],IUIAnimationVariableChangeHandler2 interface, uianimation.iuianimationvariablechangehandler2_onvaluechanged, uianimation/IUIAnimationVariableChangeHandler2::OnValueChanged
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
 - IUIAnimationVariableChangeHandler2.OnValueChanged
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
- IUIAnimationVariableChangeHandler2.OnValueChanged
: 
---

# IUIAnimationVariableChangeHandler2::OnValueChanged


## -description


Handles events that occur when the value of an animation variable changes in the specified dimension.


## -parameters




### -param storyboard [in]

The storyboard that is animating the animation variable specified by the <i>variable</i> parameter.


### -param variable [in]

The animation variable that has been updated.


### -param newValue [in]

The new value of the animation variable.


### -param previousValue [in]

The previous value of the animation variable.


### -param cDimension [in]

The dimension in which the value of the animation variable changed.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method receives updates as <b>DOUBLE</b> values.  
         To receive updates as <b>INT32</b> values, use the <a href="https://msdn.microsoft.com/76889784-BF1B-475B-8D84-201BEE6F0594">IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged</a> method.

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>IUIAnimationVariableChangeHandler2::OnValueChanged</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/7925D462-C3FD-4BD2-806D-66FE822979EF">IUIAnimationVariable2::GetValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/FF39BE67-AED7-4B67-ABAF-D5D51619F0D3">IUIAnimationVariable2::GetFinalValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1A2BF7DB-1C7B-43BF-A7F7-A4FB47250597">IUIAnimationVariable2::GetPreviousValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C878B86A-87AD-457A-802A-9A329B401B08">IUIAnimationVariable2::GetIntegerValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/290EC1D8-007D-44A0-B3F8-384A9594FDC4">IUIAnimationVariable2::GetFinalIntegerValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8B25BE8D-B12F-44B4-AFBF-3E6994BA0771">IUIAnimationVariable2::GetPreviousIntegerValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7A9B4A84-94E4-4B6C-B2FF-0A0A70397D21">IUIAnimationVariable2::GetCurrentStoryboard
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/29E6CA4D-527D-4C9D-9E28-2E2C67516126">IUIAnimationVariable2::GetTag
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ED367DB7-91D6-4D2E-BDAB-27FA4340F091">IUIAnimationManager2::GetVariableFromTag
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C7B11A34-E5FB-40D7-A655-29D28ECF4068">IUIAnimationManager2::GetStoryboardFromTag
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A73D5003-FC28-4A79-B157-3D0D2E0DEB3D">IUIAnimationStoryboard2::GetTag
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/51ae200a-a630-44fd-afd4-33d1b1dbf6d7">IUIAnimationVariable::GetValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/577f83c1-aba7-4a51-82dc-68a103a31377">IUIAnimationVariable::GetFinalValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/405bc35e-8b38-40fb-acf4-107fa6dd161a">IUIAnimationVariable::GetPreviousValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/044fd6a3-6e40-4f4f-8777-1a1a66c91989">IUIAnimationVariable::GetIntegerValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/19d71abc-e3f8-48d4-9ceb-5920dcc9c007">IUIAnimationVariable::GetFinalIntegerValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ccf4c575-aa98-40cd-b2de-cf8db95ec57d">IUIAnimationVariable::GetPreviousIntegerValue
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/56042549-d6f6-4eed-8079-c1b14acbe160">IUIAnimationVariable::GetCurrentStoryboard
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2731d302-dc52-4a10-8012-a246856d132b">IUIAnimationVariable::GetTag
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/611c5341-f225-461d-9718-a2432d796764">IUIAnimationManager::GetVariableFromTag
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/74a9265a-3602-4707-949e-6073cbde9ac4">IUIAnimationManager::GetStoryboardFromTag
</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c74dc23-ea42-400d-a78c-79b716c5e614">IUIAnimationStoryboard::GetTag
</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/F603C693-8F91-483F-8B0A-712E03BC10E5">IUIAnimationVariable2::SetVariableChangeHandler</a>



<a href="https://msdn.microsoft.com/A8D3B617-43D6-4541-AE98-1332DB5205CE">IUIAnimationVariableChangeHandler2</a>



<a href="https://msdn.microsoft.com/778BE01B-360C-431C-9515-DE43B4F2B77D">IUIAnimationVariableIntegerChangeHandler2</a>



<a href="https://msdn.microsoft.com/76889784-BF1B-475B-8D84-201BEE6F0594">IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged</a>
 

 

