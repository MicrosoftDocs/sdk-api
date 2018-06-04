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

# PFLS_CALLBACK_FUNCTION callback function


## -description


An application-defined function. If the FLS slot is in use, <b>FlsCallback</b> is called on fiber deletion, thread exit, and when an FLS index is freed. Specify this function when calling the 
<a href="https://msdn.microsoft.com/dc348ef3-37e5-40f2-bd5c-5f8aebc7cc59">FlsAlloc</a> function. The <i>PFLS_CALLBACK_FUNCTION</i> type defines a pointer to this callback function. 
<b>FlsCallback</b> is a placeholder for the application-defined function name.


## -parameters




### -param lpFlsData [in]

The value stored in the FLS slot for the calling fiber.


## -returns



This function does not return a value.




## -remarks



Each FLS index has an associated 
<b>FlsCallback</b> function. The callback function can be used for any purpose, but it is intended to be used primarily to free memory.




## -see-also




<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>



<a href="https://msdn.microsoft.com/dc348ef3-37e5-40f2-bd5c-5f8aebc7cc59">FlsAlloc</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

