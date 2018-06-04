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

# WS_ENCODER_ENCODE_CALLBACK callback function


## -description


Encodes a message.


## -parameters




### -param *encoderContext [in]


                    The encoder instance returned by the <a href="https://msdn.microsoft.com/47a68722-0c99-478a-b1ce-2982287e6a74">WS_CREATE_ENCODER_CALLBACK</a>.
                


### -param *buffers


              The buffers of data to write.
            


### -param count [in]


              The number of buffers to write.
            


### -param *asyncContext [in, optional]


                    Information on how to invoke the function asynchronously, or NULL if invoking synchronously.
                


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">

Ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks




              The encoder can use the callback passed to <a href="https://msdn.microsoft.com/47a68722-0c99-478a-b1ce-2982287e6a74">WS_CREATE_ENCODER_CALLBACK</a> to
              write the encoded data of the message.
            



