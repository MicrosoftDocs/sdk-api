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

# WS_READ_CALLBACK callback function


## -description


Used by the <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a>
        to read from some source into a buffer.
      


## -parameters




### -param *callbackState [in]

A   <b>void</b> pointer to the user-defined state value that was passed to the function that accepted this callback.


### -param *bytes

A <b>void</b> pointer to the location where the data should be placed.
        


### -param maxSize [in]

The maximum number of bytes that may be read.
        


### -param *actualSize [out]

A pointer to a <b>ULONG</b>  value that indicates the number of bytes actually read.  This may be less than maxSize.  Returning 0
          indicates that there is no more data.
        
        


### -param *asyncContext [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4">WS_ASYNC_CONTEXT</a> structure containing information on how to invoke the function asynchronously.  Assigned <b>NULL</b> if invoking synchronously.


### -param *error [in, optional]


          A pointer to <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> data structure where additional error information should be stored if the function fails.
        


## -returns



This callback function does not return a value.




## -remarks




        Returning size of 0 in the <i>actualSize</i> output parameter indicates the end of the file.
      



