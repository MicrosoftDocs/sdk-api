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

# PdhOpenQueryA function


## -description



			Creates a new query that is used to manage the collection of performance data.
			

To use handles to data sources, use the 
<a href="https://msdn.microsoft.com/068c55da-d7e0-4111-91c8-a2bbd676f99d">PdhOpenQueryH</a> function.


## -parameters




### -param szDataSource [in]

<b>Null</b>-terminated string that specifies the name of the log file from which to retrieve performance data. If <b>NULL</b>, performance data is collected from a real-time data source. 



					


### -param dwUserData [in]

User-defined value to associate with this query. To retrieve the user data later, call 
<a href="https://msdn.microsoft.com/12e1a194-5418-4c2a-9853-ef2d2c666893">PdhGetCounterInfo</a> and access the <b>dwQueryUserData</b> member of <a href="https://msdn.microsoft.com/c9ede50e-85de-4a68-b539-54285c2599cb">PDH_COUNTER_INFO</a>.


### -param phQuery [out]

Handle to the query. You use this handle in subsequent calls.


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. 




## -see-also




<a href="https://msdn.microsoft.com/af0fb9f4-3999-48fa-88d7-aa59b5caed75">PdhCloseQuery</a>



<a href="https://msdn.microsoft.com/12e1a194-5418-4c2a-9853-ef2d2c666893">PdhGetCounterInfo</a>



<a href="https://msdn.microsoft.com/4f6b2d8d-3a0f-4346-8b8e-a7aea11fbc40">PdhIsRealTimeQuery</a>



<a href="https://msdn.microsoft.com/068c55da-d7e0-4111-91c8-a2bbd676f99d">PdhOpenQueryH</a>



<a href="https://msdn.microsoft.com/5a46ac26-c1a1-40c1-a328-688e0b394e18">PdhSetDefaultRealTimeDataSource</a>
 

 

