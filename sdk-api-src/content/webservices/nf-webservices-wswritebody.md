---
UID: NF:webservices.WsWriteBody
title: WsWriteBody function
author: windows-sdk-content
description: Writes a value in the body of a message. This is a helper function that serializes a value to the XML Writer of the message. The message state must be set to WS_MESSAGE_STATE_WRITING. This function does not cause any state transitions.
old-location: wsw\wswritebody.htm
tech.root: wsw
ms.assetid: 70ff43f5-6f1a-4bbb-aa39-6fb9476e6a37
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WsWriteBody, WsWriteBody function [Web Services for Windows], webservices/WsWriteBody, wsw.wswritebody
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
 - WsWriteBody
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsWriteBody function


## -description


Writes a value in the body of a message.
            This is a helper function that serializes a value to the XML Writer 
                of the message.
            The message state must be set to <b>WS_MESSAGE_STATE_WRITING</b>.  This function
                does not cause any state transitions.
            


## -parameters




### -param message [in]

A pointer to the <b>Message</b> object for writing to.  The pointer must reference a valid <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> object.
                
                


### -param bodyDescription [in]

A pointer to information describing how to write the value.  


### -param writeOption [in]

Determines whether the value is required and how the value is allocated.
                    <div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/24a0ad2c-fcec-42c5-8f72-bea431b06d2e">WS_WRITE_OPTION</a> for more information.</div>
<div> </div>



### -param value

A void pointer to the value to write.
                


### -param valueSize [in]

The size in bytes of the value to write.
                If the value is <b>NULL</b> the size should be 0.


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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



This functions supports the following scenarios, based on the contents
                of the <a href="https://msdn.microsoft.com/17035b64-9b2c-40d3-bdce-45e9b132e9f1">WS_ELEMENT_DESCRIPTION</a> supplied:
            

<ul>
<li>Writing a single element.  In this case, the elementLocalName and elementNs
                fields of the <b>WS_ELEMENT_DESCRIPTION</b> should be set to the local name
                and namespace of the element to write, and the type and type description represents
                the type of the value being serialized.  If using <b>WS_FAULT_TYPE</b> or
                <b>WS_ENDPOINT_ADDRESS_TYPE</b>, it is not necessary to specify the local name,
                namespace, or type description (they will default appropriately based on the
                envelope/addressing version of the message).
                </li>
<li>Writing multiple elements as a single value.  In this case, the elementLocalName and elementNs
                fields of the <b>WS_ELEMENT_DESCRIPTION</b> should be set to <b>NULL</b>, and a <b>WS_STRUCT_TYPE</b>and <b>WS_STRUCT_DESCRIPTION</b> should be specified.  In this case, each field of the
                structure value being serialized should correspond to element(s) to write within the body.
                </li>
<li>Writing multiple elements as multiple values.  Writing multiple distinct values can be
                accomplished by simply calling the function multiple times.
            </li>
</ul>


