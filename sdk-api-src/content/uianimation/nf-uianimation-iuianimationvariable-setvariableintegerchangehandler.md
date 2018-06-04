---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

