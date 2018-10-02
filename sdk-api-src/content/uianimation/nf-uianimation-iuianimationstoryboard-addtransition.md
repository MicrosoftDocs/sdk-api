---
UID: NF:uianimation.IUIAnimationStoryboard.AddTransition
title: IUIAnimationStoryboard::AddTransition
author: windows-sdk-content
description: Adds a transition to the storyboard.
old-location: uianimation\iuianimationstoryboard_addtransition.htm
tech.root: UIAnimation
ms.assetid: c3213e5d-c8f5-406a-bc44-9de7a740b070
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddTransition, AddTransition method [Windows Animation], AddTransition method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],AddTransition method, IUIAnimationStoryboard.AddTransition, IUIAnimationStoryboard::AddTransition, uianimation.iuianimationstoryboard_addtransition, uianimation/IUIAnimationStoryboard::AddTransition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IUIAnimationStoryboard.AddTransition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboard::AddTransition


## -description


Adds a transition to the storyboard.


## -parameters




### -param variable [in]

The animation variable for which the transition is to be added.


### -param transition [in]

 
               The transition to be added.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_TRANSITION_ALREADY_USED</b></dt>
</dl>
</td>
<td width="60%">
This transition has already been added to a storyboard.

</td>
</tr>
</table>
 




## -remarks



The <b>AddTransition</b> method applies the specified transition to the specified variable in the storyboard. If this is the first transition applied to this variable in this storyboard, the transition begins at the start of the storyboard. Otherwise, the transition is appended to the transition that was most recently added to the variable.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/e2641c93-e520-4749-a98e-5a58c175fdb9">Create a Storyboard and Add Transitions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/055206d8-ea9e-4013-89ee-2929bfeb2731">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="https://msdn.microsoft.com/75db41ef-526b-40aa-a62d-a4262cc8d80e">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>
 

 

