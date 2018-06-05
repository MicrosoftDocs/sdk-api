---
UID: NF:uianimation.IUIAnimationManager.GetVariableFromTag
title: IUIAnimationManager::GetVariableFromTag
author: windows-sdk-content
description: Gets the animation variable with the specified tag.
old-location: uianimation\iuianimationmanager_getvariablefromtag.htm
old-project: UIAnimation
ms.assetid: 611c5341-f225-461d-9718-a2432d796764
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetVariableFromTag, GetVariableFromTag method [Windows Animation], GetVariableFromTag method [Windows Animation],IUIAnimationManager interface, IUIAnimationManager interface [Windows Animation],GetVariableFromTag method, IUIAnimationManager.GetVariableFromTag, IUIAnimationManager::GetVariableFromTag, uianimation.iuianimationmanager_getvariablefromtag, uianimation/IUIAnimationManager::GetVariableFromTag
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
-	IUIAnimationManager.GetVariableFromTag
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager::GetVariableFromTag


## -description



      Gets the animation variable with the specified tag.


## -parameters




### -param object [in, optional]


               The object portion of the tag.
            This parameter can be <b>NULL</b>.


### -param id [in]


                The identifier portion of the tag.


### -param variable [out]


               The animation variable that matches the specified tag, or <b>NULL</b> if no match is found.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks




         A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>). An application can use tags to identify animation variables and storyboards. <b>NULL</b> is a valid object component of a tag; therefore, the <i>object</i> parameter can be <b>NULL</b>.

Tags are not necessarily unique; this method returns <b>UI_E_AMBIGUOUS_MATCH</b> if more than one animation variable exists with the specified tag.




## -see-also




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>



<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>



<a href="https://msdn.microsoft.com/2731d302-dc52-4a10-8012-a246856d132b">
      IUIAnimationVariable::GetTag</a>



<a href="https://msdn.microsoft.com/176b0047-cac8-474b-9126-fdab4bc41537">
      IUIAnimationVariable::SetTag</a>
 

 

