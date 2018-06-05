---
UID: NF:uianimation.IUIAnimationTransition.IsDurationKnown
title: IUIAnimationTransition::IsDurationKnown
author: windows-sdk-content
description: Determines whether a transition's duration is currently known.
old-location: uianimation\iuianimationtransition_isdurationknown.htm
old-project: UIAnimation
ms.assetid: 5cb22573-a318-4682-bc82-0a81c9dbdcbe
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationTransition interface [Windows Animation],IsDurationKnown method, IUIAnimationTransition.IsDurationKnown, IUIAnimationTransition::IsDurationKnown, IsDurationKnown, IsDurationKnown method [Windows Animation], IsDurationKnown method [Windows Animation],IUIAnimationTransition interface, uianimation.iuianimationtransition_isdurationknown, uianimation/IUIAnimationTransition::IsDurationKnown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps | UWP apps]
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
tech.root: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationTransition.IsDurationKnown
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransition::IsDurationKnown


## -description


Determines whether a transition's duration is currently known.


## -parameters






## -returns




               Returns S_OK if the duration is known, S_FALSE if the duration is not known, or an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_STORYBOARD_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The storyboard for this transition is currently in schedule.

</td>
</tr>
</table>
 




## -remarks



This method should not be called when the storyboard to which the transition has been added is scheduled or playing.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/cc46ca31-3146-4d93-b859-79fe5e1fea08">IUIAnimationTransition::GetDuration</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/cc46ca31-3146-4d93-b859-79fe5e1fea08">IUIAnimationTransition::GetDuration</a>
 

 

