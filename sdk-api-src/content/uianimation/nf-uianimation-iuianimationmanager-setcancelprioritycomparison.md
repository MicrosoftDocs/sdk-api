---
UID: NF:uianimation.IUIAnimationManager.SetCancelPriorityComparison
title: IUIAnimationManager::SetCancelPriorityComparison (uianimation.h)
author: windows-sdk-content
description: Sets the priority comparison handler to be called to determine whether a scheduled storyboard can be canceled.
old-location: uianimation\iuianimationmanager_setcancelprioritycomparison.htm
tech.root: UIAnimation
ms.assetid: cea146d1-4a9c-4089-8015-ac16602f5afd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],SetCancelPriorityComparison method, IUIAnimationManager.SetCancelPriorityComparison, IUIAnimationManager::SetCancelPriorityComparison, SetCancelPriorityComparison, SetCancelPriorityComparison method [Windows Animation], SetCancelPriorityComparison method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_setcancelprioritycomparison, uianimation/IUIAnimationManager::SetCancelPriorityComparison
ms.topic: method
f1_keywords: 
 - "uianimation/IUIAnimationManager.SetCancelPriorityComparison"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationManager.SetCancelPriorityComparison
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationManager::SetCancelPriorityComparison


## -description


Sets the priority comparison handler to be called to determine whether a scheduled storyboard can be canceled.


## -parameters




### -param comparison [in, optional]

The priority comparison handler for cancelation.  
               
               The specified object must implement the
               <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationprioritycomparison">IUIAnimationPriorityComparison</a> interface or be <b>NULL</b>.
            See Remarks.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Setting a priority comparison handler with this method
         enables the application to indicate when scheduling conflicts can be resolved by canceling storyboards.

A scheduled storyboard can be canceled only if it has not started playing and the priority comparison object registered with this method returns <b>S_OK</b>. Canceled storyboards are completely removed from the schedule.

Passing <b>NULL</b> for the <i>comparison</i> parameter causes Windows Animation to release its reference to any priority comparison handler object you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-shutdown">IUIAnimationManager::Shutdown</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcompressprioritycomparison">IUIAnimationManager::SetCompressPriorityComparison</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setconcludeprioritycomparison">IUIAnimationManager::SetConcludePriorityComparison</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-settrimprioritycomparison">IUIAnimationManager::SetTrimPriorityComparison</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationprioritycomparison">IUIAnimationPriorityComparison</a>
 

 

