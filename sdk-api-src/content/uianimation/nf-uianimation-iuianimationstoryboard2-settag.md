---
UID: NF:uianimation.IUIAnimationStoryboard2.SetTag
title: IUIAnimationStoryboard2::SetTag
author: windows-sdk-content
description: Sets the tag for the storyboard.
old-location: uianimation\iuianimationstoryboard2_settag.htm
old-project: UIAnimation
ms.assetid: 9BEB2BF7-55F7-43F7-822C-CB4AC6F29E32
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationStoryboard2 interface [Windows Animation],SetTag method, IUIAnimationStoryboard2.SetTag, IUIAnimationStoryboard2::SetTag, SetTag, SetTag method [Windows Animation], SetTag method [Windows Animation],IUIAnimationStoryboard2 interface, uianimation.iuianimationstoryboard2_settag, uianimation/IUIAnimationStoryboard2::SetTag
ms.prod: windows
ms.technology: windows-sdk
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
-	IUIAnimationStoryboard2.SetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard2::SetTag


## -description



      Sets the tag for the storyboard.


## -parameters




### -param object [in, optional]


            The object portion of the tag.        
            This parameter can be NULL.


### -param id [in]


            The identifier portion of the tag.


## -returns



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks




         
         A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>). It can be used by an application to identify a storyboard.




## -see-also




<a href="https://msdn.microsoft.com/C7B11A34-E5FB-40D7-A655-29D28ECF4068">
      IUIAnimationManager2::GetStoryboardFromTag</a>



<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/A73D5003-FC28-4A79-B157-3D0D2E0DEB3D">
      IUIAnimationStoryboard2::GetTag</a>
 

 

