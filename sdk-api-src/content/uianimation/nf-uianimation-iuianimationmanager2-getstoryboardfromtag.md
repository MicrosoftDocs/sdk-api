---
UID: NF:uianimation.IUIAnimationManager2.GetStoryboardFromTag
title: IUIAnimationManager2::GetStoryboardFromTag method
author: windows-driver-content
description: Gets the storyboard with the specified tag.
old-location: uianimation\iuianimationmanager2_getstoryboardfromtag.htm
old-project: UIAnimation
ms.assetid: C7B11A34-E5FB-40D7-A655-29D28ECF4068
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetStoryboardFromTag method [Windows Animation], GetStoryboardFromTag method [Windows Animation], IUIAnimationManager2 interface, GetStoryboardFromTag,IUIAnimationManager2.GetStoryboardFromTag, IUIAnimationManager2, IUIAnimationManager2 interface [Windows Animation], GetStoryboardFromTag method, IUIAnimationManager2::GetStoryboardFromTag, uianimation.iuianimationmanager2_getstoryboardfromtag, uianimation/IUIAnimationManager2::GetStoryboardFromTag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps | UWP apps]
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationManager2.GetStoryboardFromTag
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager2::GetStoryboardFromTag method


## -description



      Gets the storyboard with the specified tag.


## -parameters




### -param object [in, optional]


                The object portion of the tag.
            This parameter can be NULL.


### -param id [in]


                The identifier portion of the tag.


### -param storyboard [out]


            
                The storyboard that matches the specified tag, or <b>NULL</b> if no match is found.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>). An application can use tags to identify animation variables and storyboards. NULL is a valid object component of a tag; therefore, the <i>object</i> parameter can be NULL.

Tags are not necessarily unique; this method returns UI_E_AMBIGUOUS_MATCH if more than one storyboard exists with the specified tag.




## -see-also




<a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">IUIAnimationManager2</a>



<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/9c74dc23-ea42-400d-a78c-79b716c5e614">
      IUIAnimationStoryboard::GetTag
      </a>



<a href="https://msdn.microsoft.com/ade41b03-9194-4b1a-a672-32bb48a2f5ba">
      IUIAnimationStoryboard::SetTag
      </a>
 

 

