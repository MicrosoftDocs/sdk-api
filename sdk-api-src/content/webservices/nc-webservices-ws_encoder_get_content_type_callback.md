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

# WS_ENCODER_GET_CONTENT_TYPE_CALLBACK callback function


## -description


Gets the content type of the message.
            


## -parameters




### -param *encoderContext [in]


                    The encoder instance returned by the <a href="https://msdn.microsoft.com/47a68722-0c99-478a-b1ce-2982287e6a74">WS_CREATE_ENCODER_CALLBACK</a>.
                


### -param *contentType [in]


                    The content type of the encoded message.
                


### -param *newContentType [out]


                    The callback should return the content type for the newly encoded message here.
                


### -param *contentEncoding [out]


                    The callback should return the content encoding for the encoded message here.
                


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




              The callback may inspect the content type provided, and then should return the 
              content type to use for the encoded message.
            


              The content type and content encoding returned must remain valid until the 
              callback is invoked again, or the encoder is freed.
            


              For <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a>, if a non-zero length content encoding
              is returned, the HTTP header "Content-Encoding" will be added to the message
              with this value.
            


              For other channel bindings, it is an error to return a non-zero length 
              content encoding.
            



