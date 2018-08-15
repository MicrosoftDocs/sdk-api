---
UID: NF:webservices.WsReadBody
title: WsReadBody function
author: windows-sdk-content
description: This is a helper function that deserializes a value from the XML Readerof the message. The WS_MESSAGE_STATE must be set to WS_MESSAGE_STATE_READING. This function does not cause any state transitions.
old-location: wsw\wsreadbody.htm
old-project: wsw
ms.assetid: 43ceeb1e-aeb2-4482-90f0-d7f6013b239f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WsReadBody, WsReadBody function [Web Services for Windows], webservices/WsReadBody, wsw.wsreadbody
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
 - WsReadBody
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsReadBody function


## -description


This is a helper function that deserializes a value from the XML Readerof the message.
            The <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE</a> must be set to <b>WS_MESSAGE_STATE_READING</b>.  This function does
                not cause any state transitions.
            




## -parameters




### -param message [in]

A pointer to the <b>Message</b> object to read the body from.  The pointer must reference a valid <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> object.
                
                


### -param bodyDescription [in]

A pointer to the object encapsulating the metadata that describes the mapping of the value to an element.
                


### -param readOption [in]

Determines whether the value is required and how to allocate the value.
                    See <a href="https://msdn.microsoft.com/634b057f-3121-43cc-919f-8636e67ce0d7">WS_READ_OPTION</a> for more information.
                


### -param heap [in, optional]

A pointer to the <b>Heap</b> object to read the element into.  The pointer must reference a valid <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a> object.
                


### -param value

The interpretation of the data referenced by this parameter depends on the <b>WS_READ_OPTION</b>.
                


### -param valueSize [in]

The interpretation of the value of this parameter depends on the <b>WS_READ_OPTION</b>.
                


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
                of the <b>WS_ELEMENT_DESCRIPTION</b>supplied:
            

<ul>
<li>Reading a single element.  In this case, the elementLocalName and elementNs
                fields of the <b>WS_ELEMENT_DESCRIPTION</b> should be set to the local name
                and namespace of the element to read, and the type and type description represents
                the type of the value being deserialized.  If using <b>WS_FAULT_TYPE</b>or
                <b>WS_ENDPOINT_ADDRESS_TYPE</b> it is not necessary to specify the local name,
                namespace, or type description (they will default appropriately based on the
                envelope/addressing version of the message).
                </li>
<li>Reading multiple elements as a single value.  In this case, the elementLocalName and elementNs
                fields of the <b>WS_ELEMENT_DESCRIPTION</b> should be set to <b>NULL</b>, and a <b>WS_STRUCT_TYPE</b>and <a href="https://msdn.microsoft.com/b426a07e-9993-4cea-8847-fc80e9d0b451">WS_STRUCT_DESCRIPTION</a> should be specified.  In this case, each field of the
                structure value being deserialized should correspond to element(s) to read within the body.
                </li>
<li>Reading multiple elements as multiple values.  Reading multiple distinct values can be
                accomplished by simply calling the function multiple times.
            </li>
</ul>


