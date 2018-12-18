---
UID: NC:webservices.WS_CREATE_LISTENER_CALLBACK
title: WS_CREATE_LISTENER_CALLBACK
author: windows-sdk-content
description: Handles the WsCreateListener call for a WS_CUSTOM_CHANNEL_BINDING.
old-location: wsw\ws_create_listener_callback.htm
tech.root: wsw
ms.assetid: 2d8e476d-dc68-44b4-b53b-be440a32efda
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_CREATE_LISTENER_CALLBACK, WS_CREATE_LISTENER_CALLBACK callback, WS_CREATE_LISTENER_CALLBACK callback function [Web Services for Windows], webservices/WS_CREATE_LISTENER_CALLBACK, wsw.ws_create_listener_callback
ms.topic: callback
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_CREATE_LISTENER_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_CREATE_LISTENER_CALLBACK callback function


## -description


Handles the <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> call
                for a <a href="https://msdn.microsoft.com/en-us/library/Dd401780(v=VS.85).aspx">WS_CUSTOM_CHANNEL_BINDING</a>.


## -parameters




### -param channelType [in]

The type of channel the listener listens for.
                


### -param *listenerParameters

The pointer to the value that was specified by the
                    <a href="https://msdn.microsoft.com/en-us/library/Dd401951(v=VS.85).aspx">WS_LISTENER_PROPERTY_CUSTOM_LISTENER_PARAMETERS</a>property when the custom listener is created using <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a>.
                

If the <a href="https://msdn.microsoft.com/en-us/library/Dd401951(v=VS.85).aspx">WS_LISTENER_PROPERTY_CUSTOM_LISTENER_PARAMETERS</a>property was not specified, the value will be <b>NULL</b>.
                


### -param listenerParametersSize [in]

The size in bytes of the value pointed to by listenerParameters.
                

If the <a href="https://msdn.microsoft.com/en-us/library/Dd401951(v=VS.85).aspx">WS_LISTENER_PROPERTY_CUSTOM_LISTENER_PARAMETERS</a>property was not specified, the size will be 0.
                


#### - **listenerInstance

A pointer to an allocated structure that represents
                    the listener instance.  This pointer
                    will be passed to all the other listener callbacks
                    for this particular listener instance.
                

If this callback is successful, then the <a href="https://msdn.microsoft.com/fd60ae42-5b3f-4482-b785-541f7379ab3e">WS_FREE_LISTENER_CALLBACK</a>will be used to free the listener instance.
                


### -param *error [in, optional]

Specifies where additional error information should be stored if the function fails.
                


#### - listenerInstance

A pointer to an allocated structure that represents
                    the listener instance.  This pointer
                    will be passed to all the other listener callbacks
                    for this particular listener instance.
                

If this callback is successful, then the <a href="https://msdn.microsoft.com/fd60ae42-5b3f-4482-b785-541f7379ab3e">WS_FREE_LISTENER_CALLBACK</a>will be used to free the listener instance.
                


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
 



