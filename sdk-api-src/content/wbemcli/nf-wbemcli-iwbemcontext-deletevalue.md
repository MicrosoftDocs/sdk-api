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

# IWbemContext::DeleteValue


## -description


The 
<b>IWbemContext::DeleteValue</b> method deletes a named context value created by 
<a href="https://msdn.microsoft.com/074d5ac7-aa86-44d8-99f9-959ef99a8004">IWbemContext::SetValue</a>.


## -parameters




### -param wszName




### -param lFlags [in]

Reserved. This parameter must be 0.


#### - strName [in]

Pointer to a valid <b>BSTR</b> containing the named context value to delete. The pointer is treated as read-only.


## -returns



This method returns an <b>HRESULT</b>HRESULT indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>HRESULT.




## -see-also




<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a>



<a href="https://msdn.microsoft.com/e11fff37-aeb7-41c5-8639-ca0a7a144263">IWbemContext::GetValue</a>



<a href="https://msdn.microsoft.com/074d5ac7-aa86-44d8-99f9-959ef99a8004">IWbemContext::SetValue</a>
 

 

