---
UID: NF:uianimation.IUIAnimationVariable.SetVariableIntegerChangeHandler
title: IUIAnimationVariable::SetVariableIntegerChangeHandler
author: windows-sdk-content
description: Specifies an integer variable change handler. This handler is notified of changes to the integer value of the animation variable.
old-location: uianimation\iuianimationvariable_setvariableintegerchangehandler.htm
old-project: UIAnimation
ms.assetid: 8dc20701-0808-4308-92fc-8be6c4b039ca
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IUIAnimationVariable interface [Windows Animation],SetVariableIntegerChangeHandler method, IUIAnimationVariable.SetVariableIntegerChangeHandler, IUIAnimationVariable::SetVariableIntegerChangeHandler, SetVariableIntegerChangeHandler, SetVariableIntegerChangeHandler method [Windows Animation], SetVariableIntegerChangeHandler method [Windows Animation],IUIAnimationVariable interface, uianimation.iuianimationvariable_setvariableintegerchangehandler, uianimation/IUIAnimationVariable::SetVariableIntegerChangeHandler
ms.prod: windows
ms.technology: windows-sdk
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
 - IUIAnimationVariable.SetVariableIntegerChangeHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariable::SetVariableIntegerChangeHandler


## -description



      Specifies an integer variable change handler. This handler is notified of changes to the integer value of the animation variable.


## -parameters




### -param handler [in, optional]


               An integer variable change handler.  
               
               The specified object must implement the
               <a href="https://msdn.microsoft.com/acd9ff0f-e2e4-4711-9d9c-54624f170ec6">IUIAnimationVariableIntegerChangeHandler</a> interface or be NULL.
            See Remarks.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Winodws Animation Error Codes</a> for a list of error codes.




## -remarks



Passing NULL for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="https://msdn.microsoft.com/3bcce52c-d29a-423c-ae76-eb88cbe8c8df">IUIAnimationManager::Shutdown</a> method.


<a href="https://msdn.microsoft.com/e12224a2-c8f3-45eb-a254-d624de16e12d">IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged</a> is called only if the rounded value has changed since the last update.




## -see-also




<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>



<a href="https://msdn.microsoft.com/d773a59f-10a5-41e4-92f1-af72d8d15105">IUIAnimationVariable::SetVariableChangeHandler</a>



<a href="https://msdn.microsoft.com/2288b256-aaf4-44fe-9ad1-f05ef7b0e30b">IUIAnimationVariableChangeHandler</a>
 

 

