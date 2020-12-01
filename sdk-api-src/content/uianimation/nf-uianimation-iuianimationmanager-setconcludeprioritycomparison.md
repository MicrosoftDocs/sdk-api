---
UID: NF:uianimation.IUIAnimationManager.SetConcludePriorityComparison
title: IUIAnimationManager::SetConcludePriorityComparison (uianimation.h)
description: Sets the priority comparison handler to be called to determine whether a scheduled storyboard can be concluded.
helpviewer_keywords: ["IUIAnimationManager interface [Windows Animation]","SetConcludePriorityComparison method","IUIAnimationManager.SetConcludePriorityComparison","IUIAnimationManager::SetConcludePriorityComparison","SetConcludePriorityComparison","SetConcludePriorityComparison method [Windows Animation]","SetConcludePriorityComparison method [Windows Animation]","IUIAnimationManager interface","uianimation.iuianimationmanager_setconcludeprioritycomparison","uianimation/IUIAnimationManager::SetConcludePriorityComparison"]
old-location: uianimation\iuianimationmanager_setconcludeprioritycomparison.htm
tech.root: UIAnimation
ms.assetid: 00a3d7e4-7ad2-46a8-a9c2-0e725005c00b
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],SetConcludePriorityComparison method, IUIAnimationManager.SetConcludePriorityComparison, IUIAnimationManager::SetConcludePriorityComparison, SetConcludePriorityComparison, SetConcludePriorityComparison method [Windows Animation], SetConcludePriorityComparison method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_setconcludeprioritycomparison, uianimation/IUIAnimationManager::SetConcludePriorityComparison
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
 - IUIAnimationManager::SetConcludePriorityComparison
 - uianimation/IUIAnimationManager::SetConcludePriorityComparison
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
 - IUIAnimationManager.SetConcludePriorityComparison
---

# IUIAnimationManager::SetConcludePriorityComparison


## -description

Sets the priority comparison handler to be called to determine whether a scheduled storyboard can be concluded.

## -parameters

### -param comparison [in, optional]

The priority comparison handler for conclusion. The specified object must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationprioritycomparison">IUIAnimationPriorityComparison</a> interface or be <b>NULL</b>.
            See Remarks.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Setting a priority comparison handler with this method enables the application to indicate when scheduling conflicts can be resolved by concluding the scheduled storyboard.

A scheduled storyboard can be concluded only if it contains a loop with a repetition count of <a href="/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a> and the priority comparison object registered with this method returns <b>S_OK</b>. If the storyboard is concluded, the current repetition of the loop completes, and the reminder of the storyboard then plays. 

Passing <b>NULL</b> for the <i>comparison</i> parameter causes Windows Animation to release its reference to any handler object you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-shutdown">IUIAnimationManager::Shutdown</a> method.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcancelprioritycomparison">IUIAnimationManager::SetCancelPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcompressprioritycomparison">IUIAnimationManager::SetCompressPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-settrimprioritycomparison">IUIAnimationManager::SetTrimPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationprioritycomparison">IUIAnimationPriorityComparison</a>