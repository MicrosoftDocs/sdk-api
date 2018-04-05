---
UID: NF:webservices.WsCreateMessageForChannel
title: WsCreateMessageForChannel function
author: windows-driver-content
description: Creates a message for use with a specified channel.
old-location: wsw\wscreatemessageforchannel.htm
old-project: wsw
ms.assetid: 0a4f076b-6725-45a9-8817-5dec3b647c4f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WsCreateMessageForChannel, WsCreateMessageForChannel function [Web Services for Windows], webservices/WsCreateMessageForChannel, wsw.wscreatemessageforchannel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
-	WsCreateMessageForChannel
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsCreateMessageForChannel function


## -description




                Creates a <a href="https://msdn.microsoft.com/edc810d9-7d78-4b79-8cbb-e87401f6ae41">message</a> for use with a specified <a href="https://msdn.microsoft.com/5a04580d-c89f-4505-a4b7-0724ffb788fd">channel</a>.
            




## -parameters




### -param channel [in]

Pointer to a <a href="https://msdn.microsoft.com/741636a4-5e0f-495a-bb1d-1a00cfd6f65a">WS_CHANNEL</a> structure representing the channel for the message.


### -param properties

An array of optional properties for the message. See <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a>.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).
                


### -param propertyCount [in]

The number of properties in the <i>properties</i> array.
                


### -param message


                    
                    On   success, a pointer that receives the address of the  <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> structure representing the new message.
                

When you no longer need this structure, you must free it by calling <a href="https://msdn.microsoft.com/50e08300-9445-4741-9298-bd80fc777041">WsFreeMessage</a>.


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




                In contrast to the more general  <a href="https://msdn.microsoft.com/1c48647e-9e77-4b7a-add3-e035c7f9f27e">WsCreateMessage</a> function,  <b>WsCreateMessageForChannel</b> ensures that
                the message version used is appropriate for the channel.
            



