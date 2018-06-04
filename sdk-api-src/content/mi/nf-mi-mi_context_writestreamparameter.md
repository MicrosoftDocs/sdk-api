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

# MI_Context_WriteStreamParameter function


## -description


Sends streamed parameter data to the client for a method invocation.


## -parameters




### -param self [in]

Request context.


### -param name [in]

A null-terminated string that represents the name of the method parameter to stream.


### -param value [in]

A value-type entity.


### -param type [in]


<a href="https://msdn.microsoft.com/21015eb7-9630-458e-acd8-923ee86ac2b8">MI_Type</a> object that indicates the type being 
      streamed.


### -param flags [in]

Must be 0 or 
     <b>MI_FLAG_NULL</b>.



#### MI_FLAG_NULL (0x1000000)

The end of the stream has been reached.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the 
      function return code. This can be one of the following codes.




## -remarks



Array-method out parameters can be marked as streamed, which means that instead of sending all out parameters 
    in one chunk they are streamed to the client. Streamed parameter data enables the client to display data in a 
    smoother fashion rather than having to wait until all of the data has been sent. This gives the user interface a 
    smoother, more consistent feel. The value can be an array that contains one or more elements of the specified 
    type. Call this function repeatedly to send the entire stream. If the client does not handle streamed parameters, 
    the server will cache all the results and send them to the client at once. In the case of the results being cached 
    when large result sets are generated, the provider may exceed quotas and be shutdown, meaning that methods that 
    generate very large result sets may work only with clients that support streaming.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/21015eb7-9630-458e-acd8-923ee86ac2b8">MI_Type</a>
 

 

