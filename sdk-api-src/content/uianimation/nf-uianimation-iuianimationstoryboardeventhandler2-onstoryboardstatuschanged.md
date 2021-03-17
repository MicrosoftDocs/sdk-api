---
UID: NF:uianimation.IUIAnimationStoryboardEventHandler2.OnStoryboardStatusChanged
title: IUIAnimationStoryboardEventHandler2::OnStoryboardStatusChanged (uianimation.h)
description: Handles storyboard status change events.
helpviewer_keywords: ["IUIAnimationStoryboardEventHandler2 interface [Windows Animation]","OnStoryboardStatusChanged method","IUIAnimationStoryboardEventHandler2.OnStoryboardStatusChanged","IUIAnimationStoryboardEventHandler2::OnStoryboardStatusChanged","OnStoryboardStatusChanged","OnStoryboardStatusChanged method [Windows Animation]","OnStoryboardStatusChanged method [Windows Animation]","IUIAnimationStoryboardEventHandler2 interface","uianimation.iuianimationstoryboardeventhandler2_onstoryboardstatuschanged","uianimation/IUIAnimationStoryboardEventHandler2::OnStoryboardStatusChanged"]
old-location: uianimation\iuianimationstoryboardeventhandler2_onstoryboardstatuschanged.htm
tech.root: UIAnimation
ms.assetid: 6C428A75-755D-4171-A714-83FC65A9D972
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboardEventHandler2 interface [Windows Animation],OnStoryboardStatusChanged method, IUIAnimationStoryboardEventHandler2.OnStoryboardStatusChanged, IUIAnimationStoryboardEventHandler2::OnStoryboardStatusChanged, OnStoryboardStatusChanged, OnStoryboardStatusChanged method [Windows Animation], OnStoryboardStatusChanged method [Windows Animation],IUIAnimationStoryboardEventHandler2 interface, uianimation.iuianimationstoryboardeventhandler2_onstoryboardstatuschanged, uianimation/IUIAnimationStoryboardEventHandler2::OnStoryboardStatusChanged
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationStoryboardEventHandler2::OnStoryboardStatusChanged
 - uianimation/IUIAnimationStoryboardEventHandler2::OnStoryboardStatusChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationStoryboardEventHandler2.OnStoryboardStatusChanged
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

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnStoryboardStatusChanged</b>:

<ul>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-createanimationvariable">IUIAnimationManager2::CreateAnimationVariable</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-createstoryboard">IUIAnimationManager2::CreateStoryboard</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getstoryboardfromtag">IUIAnimationManager2::GetStoryboardFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getvariablefromtag">IUIAnimationManager2::GetVariableFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-abandon">IUIAnimationStoryboard2::Abandon</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeatoffset">IUIAnimationStoryboard2::AddKeyframeAtOffset</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeaftertransition">IUIAnimationStoryboard2::AddKeyframeAfterTransition</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransition">IUIAnimationStoryboard2::AddTransition</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransitionatkeyframe">IUIAnimationStoryboard2::AddTransitionAtKeyframe</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransitionbetweenkeyframes">IUIAnimationStoryboard2::AddTransitionBetweenKeyframes</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-conclude">IUIAnimationStoryboard2::Conclude</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-finish">IUIAnimationStoryboard2::Finish</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-gettag">IUIAnimationStoryboard2::GetTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-holdvariable">IUIAnimationStoryboard2::HoldVariable</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-repeatbetweenkeyframes">IUIAnimationStoryboard2::RepeatBetweenKeyframes</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-setlongestacceptabledelay">IUIAnimationStoryboard2::SetLongestAcceptableDelay</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-setstoryboardeventhandler">IUIAnimationStoryboard2::SetStoryboardEventHandler</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-settag">IUIAnimationStoryboard2::SetTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-schedule">IUIAnimationStoryboard2::Schedule</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition2-getduration">IUIAnimationTransition2::GetDuration</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition2-isdurationknown">IUIAnimationTransition2::IsDurationKnown</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition2-setinitialvalue">IUIAnimationTransition2::SetInitialValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition2-setinitialvelocity">IUIAnimationTransition2::SetInitialVelocity</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurrentstoryboard">IUIAnimationVariable2::GetCurrentStoryboard</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getfinalintegervalue">IUIAnimationVariable2::GetFinalIntegerValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getfinalvalue">IUIAnimationVariable2::GetFinalValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getintegervalue">IUIAnimationVariable2::GetIntegerValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getpreviousintegervalue">IUIAnimationVariable2::GetPreviousIntegerValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getpreviousvalue">IUIAnimationVariable2::GetPreviousValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-gettag">IUIAnimationVariable2::GetTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getvalue">IUIAnimationVariable2::GetValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-settag">IUIAnimationVariable2::SetTag</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-getstatus">IUIAnimationStoryboard2::GetStatus</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboardeventhandler2">IUIAnimationStoryboardEventHandler2</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>