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

# IDataCollectorSet::SetValue


## -description


Sets a user-defined value.


## -parameters




### -param key




### -param value






#### - Key [in]

The name of the value. 


#### - pValue [in]

The value associated with the key. 


## -returns



Returns S_OK if successful.




## -remarks



You can specify one or more user-defined values. If you specify a key that currently exists, the current value is overwritten. To remove a value, set the <i>pValue</i> parameter to <b>NULL</b>.

You use the key value if you want to perform variable substitution in the <a href="https://msdn.microsoft.com/7bd045df-379b-40fb-b309-cec531493018">IDataCollectorSet::TaskArguments</a> property.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/0f82e154-7d3f-44c9-8bdd-cc1522499e85">IDataCollectorSet::GetValue</a>
 

 

