---
UID: NF:uianimation.IUIAnimationStoryboardEventHandler2.OnStoryboardUpdated
title: IUIAnimationStoryboardEventHandler2::OnStoryboardUpdated (uianimation.h)
description: Handles storyboard update events.
helpviewer_keywords: ["IUIAnimationStoryboardEventHandler2 interface [Windows Animation]","OnStoryboardUpdated method","IUIAnimationStoryboardEventHandler2.OnStoryboardUpdated","IUIAnimationStoryboardEventHandler2::OnStoryboardUpdated","OnStoryboardUpdated","OnStoryboardUpdated method [Windows Animation]","OnStoryboardUpdated method [Windows Animation]","IUIAnimationStoryboardEventHandler2 interface","uianimation.iuianimationstoryboardeventhandler2_onstoryboardupdated","uianimation/IUIAnimationStoryboardEventHandler2::OnStoryboardUpdated"]
old-location: uianimation\iuianimationstoryboardeventhandler2_onstoryboardupdated.htm
tech.root: UIAnimation
ms.assetid: 30AB185A-D555-47CA-A2E6-DAAEB0C56FCD
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboardEventHandler2 interface [Windows Animation],OnStoryboardUpdated method, IUIAnimationStoryboardEventHandler2.OnStoryboardUpdated, IUIAnimationStoryboardEventHandler2::OnStoryboardUpdated, OnStoryboardUpdated, OnStoryboardUpdated method [Windows Animation], OnStoryboardUpdated method [Windows Animation],IUIAnimationStoryboardEventHandler2 interface, uianimation.iuianimationstoryboardeventhandler2_onstoryboardupdated, uianimation/IUIAnimationStoryboardEventHandler2::OnStoryboardUpdated
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
 - IUIAnimationStoryboardEventHandler2::OnStoryboardUpdated
 - uianimation/IUIAnimationStoryboardEventHandler2::OnStoryboardUpdated
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
 - IUIAnimationStoryboardEventHandler2.OnStoryboardUpdated
---

# IUIAnimationStoryboardEventHandler2::OnStoryboardUpdated


## -description

Handles storyboard update events.

## -parameters

### -param storyboard [in]

The storyboard that has been updated.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method is called when the value of at least one of the variables that a storyboard is animating has changed since the last call to the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-update">IUIAnimationManager2::Update</a> method.

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnStoryboardUpdated</b>:

<ul>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getstoryboardfromtag">IUIAnimationManager2::GetStoryboardFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getvariablefromtag">IUIAnimationManager2::GetVariableFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-gettag">IUIAnimationStoryboard2::GetTag</a>
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
</ul>

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-update">IUIAnimationManager2::Update</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getelapsedtime">IUIAnimationStoryboard2::GetElapsedTime
      </a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboardeventhandler2">IUIAnimationStoryboardEventHandler2</a>