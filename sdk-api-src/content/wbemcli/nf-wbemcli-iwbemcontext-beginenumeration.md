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

# IWbemContext::BeginEnumeration


## -description


The 
<b>IWbemContext::BeginEnumeration</b> method resets the enumeration of all the context values in the object. This method must be called before the first call to 
<a href="https://msdn.microsoft.com/e316564c-a739-472b-b7a8-8acbf71e1c58">IWbemContext::Next</a> to enumerate all of the context values in the object. The order in which context values are enumerated is guaranteed to be invariant for a given instance of 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a>.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0.


## -returns



This method returns an <b>HRESULT</b>HRESULT indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>HRESULT.




## -see-also




<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a>



<a href="https://msdn.microsoft.com/bbd12aec-55ee-4cee-bf27-85f12467e06f">IWbemContext::EndEnumeration</a>



<a href="https://msdn.microsoft.com/e316564c-a739-472b-b7a8-8acbf71e1c58">IWbemContext::Next</a>
 

 

