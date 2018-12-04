---
UID: NF:webservices.WsCreateMessage
title: WsCreateMessage function
author: windows-sdk-content
description: Creates a message object with the specified properties.
old-location: wsw\wscreatemessage.htm
tech.root: wsw
ms.assetid: 1c48647e-9e77-4b7a-add3-e035c7f9f27e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsCreateMessage, WsCreateMessage function [Web Services for Windows], webservices/WsCreateMessage, wsw.wscreatemessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsCreateMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsCreateMessage function


## -description



Creates a <a href="https://msdn.microsoft.com/edc810d9-7d78-4b79-8cbb-e87401f6ae41">message</a> object with the specified properties.






## -parameters




### -param envelopeVersion [in]

A <a href="https://msdn.microsoft.com/2a6f6148-d37d-4ac2-8fd0-409eae71a3d8">WS_ENVELOPE_VERSION</a> enumeration value that specifies the version of the envelope for the message.
                


### -param addressingVersion [in]

A <a href="https://msdn.microsoft.com/87f60067-109c-456c-b060-33ab840872e0">WS_ADDRESSING_VERSION</a> that specifies the version of the addressing for the message.
                


### -param properties

An array of optional properties for the message. See <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a>.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).
                


### -param propertyCount [in]

The number of properties in the <i>properties</i> array.
                


### -param message

On   success, a pointer that receives the address of a  <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> structure representing the new message.
                

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



A message object is the delivery vehicle for Windows Web Services. A single message object can be used to send or  receive sequential messages. Reusing a message object in this way can reduce memory allocations.
            When you no longer need the message, you must free the memory by calling <a href="https://msdn.microsoft.com/50e08300-9445-4741-9298-bd80fc777041">WsFreeMessage</a>. (For more information on reusing message objects, see <a href="https://msdn.microsoft.com/90a62cc8-a7e0-4451-8490-f6384bf3e7b6">WsResetMessage</a> .)
            

If you are creating a message for use with a particular channel,  use the <a href="https://msdn.microsoft.com/0a4f076b-6725-45a9-8817-5dec3b647c4f">WsCreateMessageForChannel</a> function, which will ensure the correct message version for the channel. 





