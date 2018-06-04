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

# WS_DECODER_DECODE_CALLBACK callback function


## -description


Decodes a message.
            


## -parameters




### -param *encoderContext [in]


                    The decoder instance returned by the <a href="https://msdn.microsoft.com/85311349-5c82-4545-8a2b-d8b9e629f04d">WS_CREATE_DECODER_CALLBACK</a>.
                


### -param *buffer


              The buffer to read into.
            


### -param maxLength [in]


              The maximum number of bytes to read.
            


### -param *length [out]


                  The number of bytes read should be returned here.
              


                 The number of bytes should be set to 0 when there are no more bytes left.  This indicates
                 the end of the decoded message data, and will cause <a href="https://msdn.microsoft.com/7cf93467-84f6-4ffb-8329-bc1df119087a">WS_DECODER_END_CALLBACK</a> to
                 be invoked.
              


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







