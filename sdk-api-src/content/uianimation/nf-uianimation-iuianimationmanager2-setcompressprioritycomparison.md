---
UID: NF:uianimation.IUIAnimationManager2.SetCompressPriorityComparison
title: IUIAnimationManager2::SetCompressPriorityComparison (uianimation.h)
description: Sets the priority comparison handler that determines whether a scheduled storyboard can be compressed.
helpviewer_keywords: ["IUIAnimationManager2 interface [Windows Animation]","SetCompressPriorityComparison method","IUIAnimationManager2.SetCompressPriorityComparison","IUIAnimationManager2::SetCompressPriorityComparison","SetCompressPriorityComparison","SetCompressPriorityComparison method [Windows Animation]","SetCompressPriorityComparison method [Windows Animation]","IUIAnimationManager2 interface","uianimation.iuianimationmanager2_setcompressprioritycomparison","uianimation/IUIAnimationManager2::SetCompressPriorityComparison"]
old-location: uianimation\iuianimationmanager2_setcompressprioritycomparison.htm
tech.root: UIAnimation
ms.assetid: A754A307-AFFB-4E43-862D-C2FBC85E6C74
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],SetCompressPriorityComparison method, IUIAnimationManager2.SetCompressPriorityComparison, IUIAnimationManager2::SetCompressPriorityComparison, SetCompressPriorityComparison, SetCompressPriorityComparison method [Windows Animation], SetCompressPriorityComparison method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_setcompressprioritycomparison, uianimation/IUIAnimationManager2::SetCompressPriorityComparison
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
 - IUIAnimationManager2::SetCompressPriorityComparison
 - uianimation/IUIAnimationManager2::SetCompressPriorityComparison
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
 - IUIAnimationManager2.SetCompressPriorityComparison
---

# IUIAnimationManager2::SetCompressPriorityComparison


## -description

Sets the priority comparison handler that determines whether  a scheduled storyboard can be compressed.

## -parameters

### -param comparison [in, optional]

The priority comparison handler for compression.  
               
The specified object must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationprioritycomparison2">IUIAnimationPriorityComparison2</a> interface or be <b>NULL</b>. See Remarks for more info.

## -returns

Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Setting a priority comparison handler with this method enables the application to indicate when scheduling conflicts can be resolved by compressing  the scheduled storyboard and any other storyboards animating the same variables.

A storyboard can be compressed only if the priority comparison object registered with this method returns <b>S_OK</b> for all the other scheduled storyboards that will be affected by compression. When the storyboards are compressed, time is temporarily accelerated for affected storyboards, so they play faster.

Passing <b>NULL</b> for the <i>comparison</i> parameter causes Windows Animation to release its reference to any handler object that you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-shutdown">IUIAnimationManager2::Shutdown</a> method.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setcancelprioritycomparison">IUIAnimationManager2::SetCancelPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setconcludeprioritycomparison">IUIAnimationManager2::SetConcludePriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-settrimprioritycomparison">IUIAnimationManager2::SetTrimPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationprioritycomparison">IUIAnimationPriorityComparison</a>