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

# DrtGetSearchPathSize function


## -description


The <b>DrtGetSearchPathSize</b> function returns the size of the search path, which represents the number of nodes utilized in the search operation.


## -parameters




### -param hSearchContext [in]

Handle to the search context. This parameter is returned by the <a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a> function.


### -param pulSearchPathSize [out]

Pointer to a <b>ULONG</b> value that indicates the size of the search path. 


## -returns



This function returns S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/a795dff7-4182-42ad-b14b-142a6c1312c7">DRT_ADDRESS_LIST</a>



<a href="https://msdn.microsoft.com/dadd5f2a-2584-4046-8cdf-4d6ea97cc878">DrtGetSearchPathSize</a>
 

 

