---
UID: NF:webservices.WsCreateListener
title: WsCreateListener function
author: windows-driver-content
description: Creates a listener with the specified properties.
old-location: wsw\wscreatelistener.htm
old-project: wsw
ms.assetid: 2e592fd2-cf88-4f87-a71b-1c3416917fa7
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WsCreateListener, WsCreateListener function [Web Services for Windows], webservices/WsCreateListener, wsw.wscreatelistener
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WebServices.dll
api_name:
-	WsCreateListener
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsCreateListener function


## -description




                Creates a <a href="https://msdn.microsoft.com/fffda587-23f5-4c7a-93c5-f03d9d3fafb2">listener</a> with the specified properties.
            




## -parameters




### -param channelType [in]


                    The type of channel the listener listens for. For channel types, see the <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE</a> enumeration.


### -param channelBinding [in]


                    The channel protocol for the listener.
                For possible bindings, see the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CHANNEL_BINDING</a> enumeration.


### -param properties

Pointer to a <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure containing optional properties for the  listener.
                

For information on which properties you can specify when creating a listener, see the  <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_ID</a> enumeration. 

For information on creating a custom listener, see the Remarks section.


### -param propertyCount [in]


                    The number of properties in the <i>properties</i> array.
                


### -param securityDescription [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/b9490f00-877c-4d9f-b361-eaca343cdee0">WS_SECURITY_DESCRIPTION</a>  structure specifying the security for the listener.

If you are creating a custom channel (using the WS_CUSTOM_CHANNEL_BINDING value of the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CHANNEL_BINDING</a> enumeration), the security description must be <b>NULL</b>. See the Remarks section.


### -param listener


                    On   success, a pointer that receives the address of the  <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">WS_LISTENER</a> structure representing the new listener.
                


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

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

Insufficient memory to complete the operation.

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



When you create a custom listener (using the WS_CUSTOM_CHANNEL_BINDING value of the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CHANNEL_BINDING</a> enumeration), you can specify only the following channel properties: 

<ul>
<li>WS_LISTENER_PROPERTY_CUSTOM_LISTENER_CALLBACKS</li>
<li>WS_LISTENER_PROPERTY_CUSTOM_LISTENER_PARAMETERS</li>
</ul>(See the <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_ID</a> enumeration.) If other initial properties are required to create the custom listener, specify them by using the WS_LISTENER_PROPERTY_CUSTOM_LISTENER_PARAMETERS property. 



To pass security information to a custom listener implementation, use the WS_LISTENER_PROPERTY_CUSTOM_LISTENER_PARAMETERS value of the  <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_ID</a> enumeration.





