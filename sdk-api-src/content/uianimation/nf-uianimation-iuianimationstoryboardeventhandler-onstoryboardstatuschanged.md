---
UID: NF:uianimation.IUIAnimationStoryboardEventHandler.OnStoryboardStatusChanged
title: IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged (uianimation.h)
description: Handles events that occur when a storyboard's status changes.
helpviewer_keywords: ["IUIAnimationStoryboardEventHandler interface [Windows Animation]","OnStoryboardStatusChanged method","IUIAnimationStoryboardEventHandler.OnStoryboardStatusChanged","IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged","OnStoryboardStatusChanged","OnStoryboardStatusChanged method [Windows Animation]","OnStoryboardStatusChanged method [Windows Animation]","IUIAnimationStoryboardEventHandler interface","uianimation.iuianimationstoryboardeventhandler_onstoryboardstatuschanged","uianimation/IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged"]
old-location: uianimation\iuianimationstoryboardeventhandler_onstoryboardstatuschanged.htm
tech.root: UIAnimation
ms.assetid: e1ccf0e3-64fc-444e-a27b-1a5bc1d9d6fd
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboardEventHandler interface [Windows Animation],OnStoryboardStatusChanged method, IUIAnimationStoryboardEventHandler.OnStoryboardStatusChanged, IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged, OnStoryboardStatusChanged, OnStoryboardStatusChanged method [Windows Animation], OnStoryboardStatusChanged method [Windows Animation],IUIAnimationStoryboardEventHandler interface, uianimation.iuianimationstoryboardeventhandler_onstoryboardstatuschanged, uianimation/IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps \| UWP apps]
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
 - IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged
 - uianimation/IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged
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
 - IUIAnimationStoryboardEventHandler.OnStoryboardStatusChanged
---

# IUIAnimationStoryboardEventHandler::OnStoryboardStatusChanged


## -description

Handles events that occur when a storyboard's status changes.

## -parameters

### -param storyboard [in]

The storyboard whose status has changed.

### -param newStatus [in]

The new status.

### -param previousStatus [in]

The previous status.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnStoryboardStatusChanged</b>:

<ul>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-createanimationvariable">IUIAnimationManager::CreateAnimationVariable</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-createstoryboard">IUIAnimationManager::CreateStoryboard</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstoryboardfromtag">IUIAnimationManager::GetStoryboardFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getvariablefromtag">IUIAnimationManager::GetVariableFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-abandon">IUIAnimationStoryboard::Abandon</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset">IUIAnimationStoryboard::AddKeyframeAtOffset</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransition">IUIAnimationStoryboard::AddTransition</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionatkeyframe">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-conclude">IUIAnimationStoryboard::Conclude</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-finish">IUIAnimationStoryboard::Finish</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-gettag">IUIAnimationStoryboard::GetTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-holdvariable">IUIAnimationStoryboard::HoldVariable</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-repeatbetweenkeyframes">IUIAnimationStoryboard::RepeatBetweenKeyframes</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay">IUIAnimationStoryboard::SetLongestAcceptableDelay</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-setstoryboardeventhandler">IUIAnimationStoryboard::SetStoryboardEventHandler</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-settag">IUIAnimationStoryboard::SetTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-schedule">IUIAnimationStoryboard::Schedule</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition-getduration">IUIAnimationTransition::GetDuration</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition-isdurationknown">IUIAnimationTransition::IsDurationKnown</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition-setinitialvalue">IUIAnimationTransition::SetInitialValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition-setinitialvelocity">IUIAnimationTransition::SetInitialVelocity</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getcurrentstoryboard">IUIAnimationVariable::GetCurrentStoryboard</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalintegervalue">IUIAnimationVariable::GetFinalIntegerValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getfinalvalue">IUIAnimationVariable::GetFinalValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getintegervalue">IUIAnimationVariable::GetIntegerValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousintegervalue">IUIAnimationVariable::GetPreviousIntegerValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getpreviousvalue">IUIAnimationVariable::GetPreviousValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-gettag">IUIAnimationVariable::GetTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getvalue">IUIAnimationVariable::GetValue</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-settag">IUIAnimationVariable::SetTag</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">IUIAnimationStoryboard::GetStatus</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboardeventhandler">IUIAnimationStoryboardEventHandler</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>