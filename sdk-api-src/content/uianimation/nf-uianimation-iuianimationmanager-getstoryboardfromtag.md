---
UID: NF:uianimation.IUIAnimationManager.GetStoryboardFromTag
title: IUIAnimationManager::GetStoryboardFromTag (uianimation.h)
author: windows-sdk-content
description: Gets the storyboard with the specified tag.
old-location: uianimation\iuianimationmanager_getstoryboardfromtag.htm
tech.root: UIAnimation
ms.assetid: 74a9265a-3602-4707-949e-6073cbde9ac4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStoryboardFromTag, GetStoryboardFromTag method [Windows Animation], GetStoryboardFromTag method [Windows Animation],IUIAnimationManager interface, IUIAnimationManager interface [Windows Animation],GetStoryboardFromTag method, IUIAnimationManager.GetStoryboardFromTag, IUIAnimationManager::GetStoryboardFromTag, uianimation.iuianimationmanager_getstoryboardfromtag, uianimation/IUIAnimationManager::GetStoryboardFromTag
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
 - IUIAnimationManager.GetStoryboardFromTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationManager::GetStoryboardFromTag


## -description


Gets the storyboard with the specified tag.


## -parameters




### -param object [in, optional]

The object portion of the tag.
            This parameter can be <b>NULL</b>.


### -param id [in]

The identifier portion of the tag.


### -param storyboard [out]

The storyboard that matches the specified tag, or <b>NULL</b> if no match is found.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>). An application can use tags to identify animation variables and storyboards. <b>NULL</b> is a valid object component of a tag; therefore, the <i>object</i> parameter can be <b>NULL</b>.

Tags are not necessarily unique; this method returns UI_E_AMBIGUOUS_MATCH if more than one storyboard exists with the specified tag.




## -see-also




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>



<a href="https://msdn.microsoft.com/9c74dc23-ea42-400d-a78c-79b716c5e614">IUIAnimationStoryboard::GetTag
      </a>



<a href="https://msdn.microsoft.com/ade41b03-9194-4b1a-a672-32bb48a2f5ba">IUIAnimationStoryboard::SetTag
      </a>
 

 

