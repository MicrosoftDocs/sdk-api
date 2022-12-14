---
UID: NF:webservices.WsWriteBody
title: WsWriteBody function (webservices.h)
description: Writes a value in the body of a message. This is a helper function that serializes a value to the XML Writer of the message. The message state must be set to WS_MESSAGE_STATE_WRITING. This function does not cause any state transitions.
helpviewer_keywords: ["WsWriteBody","WsWriteBody function [Web Services for Windows]","webservices/WsWriteBody","wsw.wswritebody"]
old-location: wsw\wswritebody.htm
tech.root: wsw
ms.assetid: 70ff43f5-6f1a-4bbb-aa39-6fb9476e6a37
ms.date: 12/05/2018
ms.keywords: WsWriteBody, WsWriteBody function [Web Services for Windows], webservices/WsWriteBody, wsw.wswritebody
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsWriteBody
 - webservices/WsWriteBody
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsWriteBody
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

A pointer to the <b>Message</b> object for writing to.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> object.

### -param bodyDescription [in]

A pointer to information describing how to write the value.

### -param writeOption [in]

Determines whether the value is required and how the value is allocated.
                    <div class="alert"><b>Note</b>  See <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_OPTION</a> for more information.</div>
<div> </div>

### -param value

A void pointer to the value to write.

### -param valueSize [in]

The size in bytes of the value to write.
                If the value is <b>NULL</b> the size should be 0.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.

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
                of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_element_description">WS_ELEMENT_DESCRIPTION</a> supplied:
            

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
                fields of the <b>WS_ELEMENT_DESCRIPTION</b> should be set to <b>NULL</b>, and a <b>WS_STRUCT_TYPE</b> and <b>WS_STRUCT_DESCRIPTION</b> should be specified.  In this case, each field of the
                structure value being serialized should correspond to element(s) to write within the body.
                </li>
<li>Writing multiple elements as multiple values.  Writing multiple distinct values can be
                accomplished by simply calling the function multiple times.
            </li>
</ul>