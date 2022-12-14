---
UID: NF:uianimation.IUIAnimationManager.SetCompressPriorityComparison
title: IUIAnimationManager::SetCompressPriorityComparison (uianimation.h)
description: Sets the priority comparison handler to be called to determine whether a scheduled storyboard can be compressed.
helpviewer_keywords: ["IUIAnimationManager interface [Windows Animation]","SetCompressPriorityComparison method","IUIAnimationManager.SetCompressPriorityComparison","IUIAnimationManager::SetCompressPriorityComparison","SetCompressPriorityComparison","SetCompressPriorityComparison method [Windows Animation]","SetCompressPriorityComparison method [Windows Animation]","IUIAnimationManager interface","uianimation.iuianimationmanager_setcompressprioritycomparison","uianimation/IUIAnimationManager::SetCompressPriorityComparison"]
old-location: uianimation\iuianimationmanager_setcompressprioritycomparison.htm
tech.root: UIAnimation
ms.assetid: bf2a7782-3541-483e-8d5e-3e82693f103c
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],SetCompressPriorityComparison method, IUIAnimationManager.SetCompressPriorityComparison, IUIAnimationManager::SetCompressPriorityComparison, SetCompressPriorityComparison, SetCompressPriorityComparison method [Windows Animation], SetCompressPriorityComparison method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_setcompressprioritycomparison, uianimation/IUIAnimationManager::SetCompressPriorityComparison
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
 - IUIAnimationManager::SetCompressPriorityComparison
 - uianimation/IUIAnimationManager::SetCompressPriorityComparison
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
 - IUIAnimationManager.SetCompressPriorityComparison
---

# IUIAnimationManager::SetCompressPriorityComparison


## -description

Sets the priority comparison handler to be called to determine whether a scheduled storyboard can be compressed.

## -parameters

### -param comparison [in, optional]

The priority comparison handler for compression.  
               
The specified object must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationprioritycomparison">IUIAnimationPriorityComparison</a> interface or be <b>NULL</b>. See Remarks.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Setting a priority comparison handler with this method enables the application to indicate when the scheduling conflicts can be resolved by compressing  the scheduled storyboard and any other storyboards animating the same variables.

A storyboard can be compressed only if the priority comparison object registered with this method returns <b>S_OK</b> for all the other scheduled storyboards that will be affected by compression. When the storyboards are compressed, time is temporarily accelerated for affected storyboards, so they play faster.

Passing <b>NULL</b> for the <i>comparison</i> parameter causes Windows Animation to release its reference to any handler object you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-shutdown">IUIAnimationManager::Shutdown</a> method.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcancelprioritycomparison">IUIAnimationManager::SetCancelPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setconcludeprioritycomparison">IUIAnimationManager::SetConcludePriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-settrimprioritycomparison">IUIAnimationManager::SetTrimPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationprioritycomparison">IUIAnimationPriorityComparison</a>