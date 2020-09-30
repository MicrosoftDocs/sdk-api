---
UID: NF:uianimation.IUIAnimationStoryboardEventHandler.OnStoryboardUpdated
title: IUIAnimationStoryboardEventHandler::OnStoryboardUpdated (uianimation.h)
description: Handles events that occur when a storyboard is updated.
helpviewer_keywords: ["IUIAnimationStoryboardEventHandler interface [Windows Animation]","OnStoryboardUpdated method","IUIAnimationStoryboardEventHandler.OnStoryboardUpdated","IUIAnimationStoryboardEventHandler::OnStoryboardUpdated","OnStoryboardUpdated","OnStoryboardUpdated method [Windows Animation]","OnStoryboardUpdated method [Windows Animation]","IUIAnimationStoryboardEventHandler interface","uianimation.iuianimationstoryboardeventhandler_onstoryboardupdated","uianimation/IUIAnimationStoryboardEventHandler::OnStoryboardUpdated"]
old-location: uianimation\iuianimationstoryboardeventhandler_onstoryboardupdated.htm
tech.root: UIAnimation
ms.assetid: e1a6349e-9c3f-49e5-8e50-b51bf260e9be
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboardEventHandler interface [Windows Animation],OnStoryboardUpdated method, IUIAnimationStoryboardEventHandler.OnStoryboardUpdated, IUIAnimationStoryboardEventHandler::OnStoryboardUpdated, OnStoryboardUpdated, OnStoryboardUpdated method [Windows Animation], OnStoryboardUpdated method [Windows Animation],IUIAnimationStoryboardEventHandler interface, uianimation.iuianimationstoryboardeventhandler_onstoryboardupdated, uianimation/IUIAnimationStoryboardEventHandler::OnStoryboardUpdated
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
 - IUIAnimationStoryboardEventHandler::OnStoryboardUpdated
 - uianimation/IUIAnimationStoryboardEventHandler::OnStoryboardUpdated
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
 - IUIAnimationStoryboardEventHandler.OnStoryboardUpdated
---

# IUIAnimationStoryboardEventHandler::OnStoryboardUpdated


## -description

Handles events that occur when a storyboard is updated.

## -parameters

### -param storyboard [in]

The storyboard that has been updated.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method is called when the value of at least one of the variables that a storyboard is animating has changed since the last call to the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-update">IUIAnimationManager::Update</a> method.

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnStoryboardUpdated</b>:

<ul>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstoryboardfromtag">IUIAnimationManager::GetStoryboardFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getvariablefromtag">IUIAnimationManager::GetVariableFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-gettag">IUIAnimationStoryboard::GetTag</a>
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
</ul>

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-update">IUIAnimationManager::Update</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getelapsedtime">IUIAnimationStoryboard::GetElapsedTime
      </a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboardeventhandler">IUIAnimationStoryboardEventHandler</a>