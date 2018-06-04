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

# WS_CREATE_ENCODER_CALLBACK callback function


## -description


Handles creating an encoder instance.


## -parameters




### -param *createContext [in]


                    The createContext that was specified in the <a href="https://msdn.microsoft.com/94ff7082-5cc7-46f3-8eec-d38565bbdb23">WS_CHANNEL_ENCODER</a>
                    used during channel creation.
                


### -param writeCallback [in]


                  The function that should be used to write the message data.  This callback
                  should only be used in response to the <a href="https://msdn.microsoft.com/308e3d24-e3df-4dc8-a727-d3d8ebe8d5d4">WS_ENCODER_START_CALLBACK</a>,
                  <a href="https://msdn.microsoft.com/f3b191b2-a92f-491d-bd77-500e2d3b37e8">WS_ENCODER_ENCODE_CALLBACK</a> and <a href="https://msdn.microsoft.com/ab0f88f7-e2b4-48e0-9041-ac4aa66f1575">WS_ENCODER_END_CALLBACK</a>
                  callbacks.
                


### -param *writeContext [in]


                    The write context that should be passed to the provided <a href="https://msdn.microsoft.com/8d106ac2-226d-4e0c-8f14-8d3e17f15548">WS_WRITE_CALLBACK</a>.
                


#### - **encoderContext


                    Returns the encoder instance.  This value will be
                    passed to all of the encoder callbacks.
                


### -param *error [in, optional]


                    Specifies where additional error information should be stored if the function fails.
                


#### - encoderContext


                    Returns the encoder instance.  This value will be
                    passed to all of the encoder callbacks.
                


## -returns



This callback function can return one of these values.

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




              The channel will create encoder instances as necessary.  Each encoder
              instance will be called in a single-threaded fashion.  A single encoder
              instance however should not assume that it will see all messages from a
              channel, as the channel may use multiple encoder instances for processing
              messages.
            



