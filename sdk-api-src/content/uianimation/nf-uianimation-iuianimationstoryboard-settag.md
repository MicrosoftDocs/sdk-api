---
UID: NF:uianimation.IUIAnimationStoryboard.SetTag
title: IUIAnimationStoryboard::SetTag
author: windows-sdk-content
description: Sets the tag for the storyboard.
old-location: uianimation\iuianimationstoryboard_settag.htm
old-project: UIAnimation
ms.assetid: ade41b03-9194-4b1a-a672-32bb48a2f5ba
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationStoryboard interface [Windows Animation],SetTag method, IUIAnimationStoryboard.SetTag, IUIAnimationStoryboard::SetTag, SetTag, SetTag method [Windows Animation], SetTag method [Windows Animation],IUIAnimationStoryboard interface, uianimation.iuianimationstoryboard_settag, uianimation/IUIAnimationStoryboard::SetTag
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationStoryboard.SetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard::SetTag


## -description



      Sets the tag for the storyboard.


## -parameters




### -param object [in, optional]


            The object portion of the tag.        
            This parameter can be <b>NULL</b>.


### -param id [in]


            The identifier portion of the tag.


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
<dt><b>UI_E_STORYBOARD_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The storyboard is currently in the schedule.

</td>
</tr>
</table>
 




## -remarks




         
         A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>); it can be used by an application to identify a storyboard.




## -see-also




<a href="https://msdn.microsoft.com/74a9265a-3602-4707-949e-6073cbde9ac4">
      IUIAnimationManager::GetStoryboardFromTag</a>



<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/9c74dc23-ea42-400d-a78c-79b716c5e614">
      IUIAnimationStoryboard::GetTag</a>
 

 

