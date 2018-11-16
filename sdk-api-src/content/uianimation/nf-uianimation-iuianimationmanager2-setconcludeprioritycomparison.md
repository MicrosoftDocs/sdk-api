---
UID: NF:uianimation.IUIAnimationManager2.SetConcludePriorityComparison
title: IUIAnimationManager2::SetConcludePriorityComparison
author: windows-sdk-content
description: Sets the priority comparison handler that determines whether a scheduled storyboard can be concluded.
old-location: uianimation\iuianimationmanager2_setconcludeprioritycomparison.htm
tech.root: UIAnimation
ms.assetid: 1BDC9094-6020-4640-B959-59CD6CF48751
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],SetConcludePriorityComparison method, IUIAnimationManager2.SetConcludePriorityComparison, IUIAnimationManager2::SetConcludePriorityComparison, SetConcludePriorityComparison, SetConcludePriorityComparison method [Windows Animation], SetConcludePriorityComparison method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_setconcludeprioritycomparison, uianimation/IUIAnimationManager2::SetConcludePriorityComparison
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IUIAnimationManager2.SetConcludePriorityComparison
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uianimation.h
: 
- IUIAnimationManager2.SetConcludePriorityComparison
: 
---

# IUIAnimationManager2::SetConcludePriorityComparison


## -description


Sets the priority comparison handler that determines whether  a scheduled storyboard can be concluded.


## -parameters




### -param comparison [in, optional]

The priority comparison handler for conclusion. The specified object must implement the <a href="https://msdn.microsoft.com/B19E9BAF-A91E-4A58-A6F0-058B03153D10">IUIAnimationPriorityComparison2</a> interface or be <b>NULL</b>.
            See Remarks for more info.


## -returns



Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Setting a priority comparison handler with this method enables the application to indicate when scheduling conflicts can be resolved by concluding the scheduled storyboard.

A scheduled storyboard can be concluded only if it contains a loop with a repetition count of <a href="https://msdn.microsoft.com/09213B74-16C9-48F9-9626-59FF6CFDE975">UI_ANIMATION_REPEAT_INDEFINITELY</a> and the priority comparison object registered with this method returns <b>S_OK</b>. If the storyboard is concluded, the current repetition of the loop completes, and the rest of the storyboard then plays. 

Passing <b>NULL</b> for the <i>comparison</i> parameter causes Windows Animation to release its reference to any handler object that you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="https://msdn.microsoft.com/F66A987C-E020-4CD6-BE3F-440C3F8B8CF2">IUIAnimationManager2::Shutdown</a> method.




## -see-also




<a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">IUIAnimationManager2</a>



<a href="https://msdn.microsoft.com/55DEC4C2-A6F3-459D-BDCD-3D3819EBF0D2">IUIAnimationManager2::SetCancelPriorityComparison</a>



<a href="https://msdn.microsoft.com/A754A307-AFFB-4E43-862D-C2FBC85E6C74">IUIAnimationManager2::SetCompressPriorityComparison</a>



<a href="https://msdn.microsoft.com/742BCD19-FC1D-46DE-9CBC-716793259947">IUIAnimationManager2::SetTrimPriorityComparison</a>



<a href="https://msdn.microsoft.com/65311cf0-f8d4-4d2c-bd4d-585ae5d921df">IUIAnimationPriorityComparison</a>
 

 

