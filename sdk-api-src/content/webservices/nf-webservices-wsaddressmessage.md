---
UID: NF:webservices.WsAddressMessage
title: WsAddressMessage function
author: windows-sdk-content
description: Addresses a message to a specified endpoint address.
old-location: wsw\wsaddressmessage.htm
old-project: wsw
ms.assetid: 30b2dbd1-7232-4ff1-b30a-920df8bfe423
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WsAddressMessage, WsAddressMessage function [Web Services for Windows], webservices/WsAddressMessage, wsw.wsaddressmessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsAddressMessage
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsAddressMessage function


## -description



Addresses a <a href="https://msdn.microsoft.com/edc810d9-7d78-4b79-8cbb-e87401f6ae41">message</a> to a specified <a href="https://msdn.microsoft.com/5df9c0da-6648-42a0-ae87-06844461042a">endpoint address</a>. 




## -parameters




### -param message [in]

Pointer to a <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> structure respresenting the  message to be addressed.


### -param address [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/4e9b5f3e-849f-46aa-a94a-3cd6ae16275f">WS_ENDPOINT_ADDRESS</a> structure containing the endpoint  to which to address the message.

<div class="alert"><b>Note</b>  Passing <b>NULL</b> to this parameter indicates that no headers are added to the message.  This provides
                    a way to set the <a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_ID</a> to <b>WS_MESSAGE_PROPERTY_IS_ADDRESSED</b> 
                    without modifying the set of headers in the message.
                </div>
<div> </div>

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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The message has already been addressed.
                    (The <b>WS_MESSAGE_PROPERTY_IS_ADDRESSED</b> property
                    indicates whether a message has already been addressed.)
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

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
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function can return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks



If you do not address a message by calling  this function, the <a href="https://msdn.microsoft.com/5a04580d-c89f-4505-a4b7-0724ffb788fd">channel</a> automatically addresses the message with the
                <a href="https://msdn.microsoft.com/5df9c0da-6648-42a0-ae87-06844461042a">Endpoint Address</a> passed to <a href="https://msdn.microsoft.com/a7226194-0974-4f3c-b92d-78a93e86eea5">WsOpenChannel</a>.

This function marks the message as addressed by setting
                the  <b>WS_MESSAGE_PROPERTY_IS_ADDRESSED</b> property  to <b>TRUE</b>.
            

This function fails 
                if the message has already been addressed and returns <b>WS_E_INVALID_OPERATION</b>.
            

If a non-<b>NULL</b><a href="https://msdn.microsoft.com/4e9b5f3e-849f-46aa-a94a-3cd6ae16275f">WS_ENDPOINT_ADDRESS</a> is passed
                to the function,  the function performs the following
                additional steps:
            

<ul>
<li>The header type is set to WS_TO_HEADER (see the <a href="https://msdn.microsoft.com/4c9b927d-00c7-41e4-bc29-e84a4c23c162">WS_HEADER_TYPE</a> enumeration) and the address is set to the value of the <b>url</b>field of <a href="https://msdn.microsoft.com/4e9b5f3e-849f-46aa-a94a-3cd6ae16275f">WS_ENDPOINT_ADDRESS</a>.  If the URL length
                is zero the <a href="https://msdn.microsoft.com/87f60067-109c-456c-b060-33ab840872e0">WS_ADDRESSING_VERSION</a>-specific 
                representation for an anonymous URL is set for the message.
                </li>
<li>Each header in the <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> specified in the 
                headers field of the <a href="https://msdn.microsoft.com/4e9b5f3e-849f-46aa-a94a-3cd6ae16275f">WS_ENDPOINT_ADDRESS</a> is added to
                the message.  No headers are added if the buffer is <b>NULL</b>.
            </li>
</ul>


