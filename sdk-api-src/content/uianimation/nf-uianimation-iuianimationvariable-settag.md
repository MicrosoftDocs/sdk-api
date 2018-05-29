---
UID: NF:uianimation.IUIAnimationVariable.SetTag
title: IUIAnimationVariable::SetTag
author: windows-sdk-content
description: Sets the tag for an animation variable.
old-location: uianimation\iuianimationvariable_settag.htm
old-project: UIAnimation
ms.assetid: 176b0047-cac8-474b-9126-fdab4bc41537
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationVariable interface [Windows Animation],SetTag method, IUIAnimationVariable.SetTag, IUIAnimationVariable::SetTag, SetTag, SetTag method [Windows Animation], SetTag method [Windows Animation],IUIAnimationVariable interface, uianimation.iuianimationvariable_settag, uianimation/IUIAnimationVariable::SetTag
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationVariable.SetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariable::SetTag


## -description



      Sets the tag for an animation variable.


## -parameters




### -param object [in, optional]


               The object portion of the tag.
            This parameter can be <b>NULL</b>.


### -param id [in]


               The identifier portion  of the tag.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks




         A tag is a pairing of an integer identifier (<i>id</i>) with a COM object (<i>object</i>); it can be used by an application to identify an animation variable.          
         Because <b>NULL</b> is a valid object component of a tag, the <i>object</i> parameter can be <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/611c5341-f225-461d-9718-a2432d796764">
      IUIAnimationManager::GetVariableFromTag</a>



<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>



<a href="https://msdn.microsoft.com/2731d302-dc52-4a10-8012-a246856d132b">IUIAnimationVariable::GetTag</a>
 

 

