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

# IUIAnimationVariable2::SetVariableIntegerChangeHandler


## -description


Specifies a handler for changes to the integer value of the animation variable. 


## -parameters




### -param handler [in, optional]

A pointer to the handler for changes to the integer value of the animation variable. This parameter can be <b>NULL</b>.




### -param fRegisterForNextAnimationEvent [in]

If <b>TRUE</b>, specifies that the <a href="https://msdn.microsoft.com/C2F049B7-287F-4EC2-A737-965E01515056">EstimateNextEventTime</a> method will incorporate <i>handler</i> into its estimate of the time interval until the next animation event. No default value.


## -returns



Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Passing <b>NULL</b> for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object that you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method.


<a href="https://msdn.microsoft.com/76889784-BF1B-475B-8D84-201BEE6F0594">IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged</a> is called only if the rounded value has changed since the last update.




## -see-also




<a href="https://msdn.microsoft.com/A676EF27-B59D-4D2D-AD5B-8F46EE337E69">IUIAnimationVariable2</a>



<a href="https://msdn.microsoft.com/A8D3B617-43D6-4541-AE98-1332DB5205CE">IUIAnimationVariableChangeHandler2</a>
 

 

