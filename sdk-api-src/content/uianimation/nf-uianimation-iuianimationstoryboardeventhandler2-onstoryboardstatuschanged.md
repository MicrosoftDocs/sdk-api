---
UID: NF:uianimation.IUIAnimationStoryboardEventHandler2.OnStoryboardStatusChanged
title: IUIAnimationStoryboardEventHandler2::OnStoryboardStatusChanged (uianimation.h)
author: windows-sdk-content
description: Handles storyboard status change events.
old-location: uianimation\iuianimationstoryboardeventhandler2_onstoryboardstatuschanged.htm
tech.root: UIAnimation
ms.assetid: 6C428A75-755D-4171-A714-83FC65A9D972
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboardEventHandler2 interface [Windows Animation],OnStoryboardStatusChanged method, IUIAnimationStoryboardEventHandler2.OnStoryboardStatusChanged, IUIAnimationStoryboardEventHandler2::OnStoryboardStatusChanged, OnStoryboardStatusChanged, OnStoryboardStatusChanged method [Windows Animation], OnStoryboardStatusChanged method [Windows Animation],IUIAnimationStoryboardEventHandler2 interface, uianimation.iuianimationstoryboardeventhandler2_onstoryboardstatuschanged, uianimation/IUIAnimationStoryboardEventHandler2::OnStoryboardStatusChanged
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
 - IUIAnimationStoryboardEventHandler2.OnStoryboardStatusChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboardEventHandler2::OnStoryboardStatusChanged


## -description


Handles storyboard status change events.


## -parameters




### -param storyboard [in]

The storyboard for which the status has changed.


### -param newStatus [in]

The new status.


### -param previousStatus [in]

The previous status.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnStoryboardStatusChanged</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/5E963D24-2436-4B8F-8806-69E521EC83AF">IUIAnimationManager2::CreateAnimationVariable</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3D66B9DC-15F0-4660-ACF5-FBC801467FD9">IUIAnimationManager2::CreateStoryboard</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C7B11A34-E5FB-40D7-A655-29D28ECF4068">IUIAnimationManager2::GetStoryboardFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ED367DB7-91D6-4D2E-BDAB-27FA4340F091">IUIAnimationManager2::GetVariableFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ABB7184F-A703-45E3-96D8-E3062EEB9565">IUIAnimationStoryboard2::Abandon</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6AB47BC1-4437-4191-8B66-8545EB4102A9">IUIAnimationStoryboard2::AddKeyframeAtOffset</a>
</li>
<li>
<a href="https://msdn.microsoft.com/F5D13D36-1AEE-4D47-9683-A428E9ADF1D6">IUIAnimationStoryboard2::AddKeyframeAfterTransition</a>
</li>
<li>
<a href="https://msdn.microsoft.com/BFC05D67-EE1C-489E-9A8C-10F0AAB24A0A">IUIAnimationStoryboard2::AddTransition</a>
</li>
<li>
<a href="https://msdn.microsoft.com/F4DAB833-E857-4FD8-87E2-8F32AF460F90">IUIAnimationStoryboard2::AddTransitionAtKeyframe</a>
</li>
<li>
<a href="https://msdn.microsoft.com/55AEA5EA-7D9E-4669-8315-7A6F4428EDF9">IUIAnimationStoryboard2::AddTransitionBetweenKeyframes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C7687E52-433F-4E73-910D-86298E528F7B">IUIAnimationStoryboard2::Conclude</a>
</li>
<li>
<a href="https://msdn.microsoft.com/632BC77D-F2C5-4D08-8E9C-0598617A1DA7">IUIAnimationStoryboard2::Finish</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A73D5003-FC28-4A79-B157-3D0D2E0DEB3D">IUIAnimationStoryboard2::GetTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/E6B7C4F9-2377-4968-A16F-15F174EC5439">IUIAnimationStoryboard2::HoldVariable</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31BC2628-14B3-4405-BA9B-4FB275D9AC0D">IUIAnimationStoryboard2::RepeatBetweenKeyframes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/D23F4833-413C-470B-8572-2DCB051576A3">IUIAnimationStoryboard2::SetLongestAcceptableDelay</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9C105DDC-4BED-45FC-B4AE-2331A228BB86">IUIAnimationStoryboard2::SetStoryboardEventHandler</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9BEB2BF7-55F7-43F7-822C-CB4AC6F29E32">IUIAnimationStoryboard2::SetTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9F20AE4A-F693-4DDA-90F4-FCCA5291208B">IUIAnimationStoryboard2::Schedule</a>
</li>
<li>
<a href="https://msdn.microsoft.com/07B5C7D7-80B1-4458-93A7-39F61121B618">IUIAnimationTransition2::GetDuration</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A73065A7-B191-4CB9-A75A-827CFC040C92">IUIAnimationTransition2::IsDurationKnown</a>
</li>
<li>
<a href="https://msdn.microsoft.com/813224BE-369D-4D65-AA12-AEE590627F40">IUIAnimationTransition2::SetInitialValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1CE8A3BD-9DDC-4FDE-BE2B-29804B3754B1">IUIAnimationTransition2::SetInitialVelocity</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7A9B4A84-94E4-4B6C-B2FF-0A0A70397D21">IUIAnimationVariable2::GetCurrentStoryboard</a>
</li>
<li>
<a href="https://msdn.microsoft.com/290EC1D8-007D-44A0-B3F8-384A9594FDC4">IUIAnimationVariable2::GetFinalIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/FF39BE67-AED7-4B67-ABAF-D5D51619F0D3">IUIAnimationVariable2::GetFinalValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C878B86A-87AD-457A-802A-9A329B401B08">IUIAnimationVariable2::GetIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8B25BE8D-B12F-44B4-AFBF-3E6994BA0771">IUIAnimationVariable2::GetPreviousIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1A2BF7DB-1C7B-43BF-A7F7-A4FB47250597">IUIAnimationVariable2::GetPreviousValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/29E6CA4D-527D-4C9D-9E28-2E2C67516126">IUIAnimationVariable2::GetTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7925D462-C3FD-4BD2-806D-66FE822979EF">IUIAnimationVariable2::GetValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/21BAFF23-8866-432F-BB9A-0328CE0E6021">IUIAnimationVariable2::SetTag</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/1694B720-891A-4214-A009-6AA722E5B83D">IUIAnimationStoryboard2::GetStatus</a>



<a href="https://msdn.microsoft.com/2AB8C0C5-2203-4778-BBEA-6D52B727FDDB">IUIAnimationStoryboardEventHandler2</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371971(v=VS.85).aspx">UI_ANIMATION_STORYBOARD_STATUS</a>
 

 

