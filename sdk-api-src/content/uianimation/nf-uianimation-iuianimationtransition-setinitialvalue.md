---
UID: NF:uianimation.IUIAnimationTransition.SetInitialValue
title: IUIAnimationTransition::SetInitialValue (uianimation.h)
author: windows-sdk-content
description: Sets the initial value for the transition.
old-location: uianimation\iuianimationtransition_setinitialvalue.htm
tech.root: UIAnimation
ms.assetid: 5e931eee-8b28-4be2-a760-8f62b5ce89ed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransition interface [Windows Animation],SetInitialValue method, IUIAnimationTransition.SetInitialValue, IUIAnimationTransition::SetInitialValue, SetInitialValue, SetInitialValue method [Windows Animation], SetInitialValue method [Windows Animation],IUIAnimationTransition interface, uianimation.iuianimationtransition_setinitialvalue, uianimation/IUIAnimationTransition::SetInitialValue
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
 - IUIAnimationTransition.SetInitialValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationTransition::SetInitialValue


## -description


Sets the initial value for the transition.


## -parameters




### -param value [in]

The initial value for the transition.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method should not be called after the transition has been added to a storyboard.



