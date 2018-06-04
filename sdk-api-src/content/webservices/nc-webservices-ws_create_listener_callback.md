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

# WS_CREATE_LISTENER_CALLBACK callback function


## -description


Handles the <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> call
                for a <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>.


## -parameters




### -param channelType [in]


                    The type of channel the listener listens for.
                


### -param *listenerParameters


                    The pointer to the value that was specified by the
                    <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_CUSTOM_LISTENER_PARAMETERS</a>
                    property when the custom listener is created using <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a>.
                


                    If the <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_CUSTOM_LISTENER_PARAMETERS</a>
                    property was not specified, the value will be <b>NULL</b>.
                


### -param listenerParametersSize [in]


                    The size in bytes of the value pointed to by listenerParameters.
                


                    If the <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_CUSTOM_LISTENER_PARAMETERS</a>
                    property was not specified, the size will be 0.
                


#### - **listenerInstance


                    A pointer to an allocated structure that represents
                    the listener instance.  This pointer
                    will be passed to all the other listener callbacks
                    for this particular listener instance.
                


                    If this callback is successful, then the <a href="https://msdn.microsoft.com/fd60ae42-5b3f-4482-b785-541f7379ab3e">WS_FREE_LISTENER_CALLBACK</a>
                    will be used to free the listener instance.
                


### -param *error [in, optional]


                    Specifies where additional error information should be stored if the function fails.
                


#### - listenerInstance


                    A pointer to an allocated structure that represents
                    the listener instance.  This pointer
                    will be passed to all the other listener callbacks
                    for this particular listener instance.
                


                    If this callback is successful, then the <a href="https://msdn.microsoft.com/fd60ae42-5b3f-4482-b785-541f7379ab3e">WS_FREE_LISTENER_CALLBACK</a>
                    will be used to free the listener instance.
                


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">

A quota was exceeded.

</td>
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
 



