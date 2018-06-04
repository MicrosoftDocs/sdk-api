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

# WS_PULL_BYTES_CALLBACK callback function


## -description


Used by the <a href="https://msdn.microsoft.com/39e25db6-e51f-45cb-9739-260e7c246fcc">WsPullBytes</a> function to request 
        the data that should be written.
      


## -parameters




### -param *callbackState [in]


          The user-defined state that was passed to <a href="https://msdn.microsoft.com/39e25db6-e51f-45cb-9739-260e7c246fcc">WsPullBytes</a>.
        


### -param *bytes


          Where the data that is read should be placed.
        


### -param maxSize [in]


          The maximum number of bytes that may be read.
        


### -param *actualSize [out]


          The actual number of bytes that were read.  This may be less than maxSize.  Returning 0
          indicates that there is no more data.
        


### -param *asyncContext [in, optional]

Information on how to invoke the function asynchronously, or <b>NULL</b> if invoking synchronously.


### -param *error [in, optional]


          Specifies where additional error information should be stored if the function fails.
        


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">

          The asynchronous operation is still pending.
        

</td>
</tr>
</table>
 




## -remarks




        Returning size of 0 indicates EOF.
      



