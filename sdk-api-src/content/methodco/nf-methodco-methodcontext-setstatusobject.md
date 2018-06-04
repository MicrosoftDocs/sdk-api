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

# MethodContext::SetStatusObject


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aea20c9d-4042-426a-abdf-51ebddf017aa">MethodContext</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetStatusObject</b> method sets an internal pointer to <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.


## -parameters




### -param pObj

A pointer to <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> information.


## -returns



<b>TRUE</b> if the call method call was successful. <b>FALSE</b> if the object has already been set.




## -see-also




<a href="https://msdn.microsoft.com/aea20c9d-4042-426a-abdf-51ebddf017aa">MethodContext</a>
 

 

