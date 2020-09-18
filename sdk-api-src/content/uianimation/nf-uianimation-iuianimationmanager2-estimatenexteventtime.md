---
UID: NF:uianimation.IUIAnimationManager2.EstimateNextEventTime
title: IUIAnimationManager2::EstimateNextEventTime (uianimation.h)
description: Retrieves an estimate of the time interval before the next animation event.
helpviewer_keywords: ["EstimateNextEventTime","EstimateNextEventTime method [Windows Animation]","EstimateNextEventTime method [Windows Animation]","IUIAnimationManager2 interface","IUIAnimationManager2 interface [Windows Animation]","EstimateNextEventTime method","IUIAnimationManager2.EstimateNextEventTime","IUIAnimationManager2::EstimateNextEventTime","uianimation.iuianimationmanager2_estimatenexteventtime","uianimation/IUIAnimationManager2::EstimateNextEventTime"]
old-location: uianimation\iuianimationmanager2_estimatenexteventtime.htm
tech.root: UIAnimation
ms.assetid: C2F049B7-287F-4EC2-A737-965E01515056
ms.date: 12/05/2018
ms.keywords: EstimateNextEventTime, EstimateNextEventTime method [Windows Animation], EstimateNextEventTime method [Windows Animation],IUIAnimationManager2 interface, IUIAnimationManager2 interface [Windows Animation],EstimateNextEventTime method, IUIAnimationManager2.EstimateNextEventTime, IUIAnimationManager2::EstimateNextEventTime, uianimation.iuianimationmanager2_estimatenexteventtime, uianimation/IUIAnimationManager2::EstimateNextEventTime
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationManager2::EstimateNextEventTime
 - uianimation/IUIAnimationManager2::EstimateNextEventTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.h
api_name:
 - IUIAnimationManager2.EstimateNextEventTime
---

# IUIAnimationManager2::EstimateNextEventTime


## -description

Retrieves an estimate of  the time interval before the next animation event.

## -parameters

### -param seconds [out]

The estimated time, in seconds.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="/windows/desktop/UIAnimation/ui-animation-seconds-infinite">UI_ANIMATION_SECONDS_INFINITE
</a>