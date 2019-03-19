---
UID: NF:uianimation.IUIAnimationStoryboard.GetTag
title: IUIAnimationStoryboard::GetTag (uianimation.h)
author: windows-sdk-content
description: Gets the tag for a storyboard.
old-location: uianimation\iuianimationstoryboard_gettag.htm
tech.root: UIAnimation
ms.assetid: 9c74dc23-ea42-400d-a78c-79b716c5e614
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTag, GetTag method [Windows Animation], GetTag method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],GetTag method, IUIAnimationStoryboard.GetTag, IUIAnimationStoryboard::GetTag, uianimation.iuianimationstoryboard_gettag, uianimation/IUIAnimationStoryboard::GetTag
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
 - IUIAnimationStoryboard.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboard::GetTag


## -description


Gets the tag for a storyboard.


## -parameters




### -param object [out, optional]

The object portion of the tag.


### -param id [out, optional]

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
<dt><b>UI_E_VALUE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The storyboard's tag was not set.

</td>
</tr>
</table>
 




## -remarks



A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>); it can be used by an application to identify a storyboard.

The parameters are optional so that the method can return both portions of the tag, or just the identifier or object portion.




## -see-also




<a href="https://msdn.microsoft.com/74a9265a-3602-4707-949e-6073cbde9ac4">IUIAnimationManager::GetStoryboardFromTag</a>



<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/ade41b03-9194-4b1a-a672-32bb48a2f5ba">IUIAnimationStoryboard::SetTag</a>
 

 

