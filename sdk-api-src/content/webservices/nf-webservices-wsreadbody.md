---
UID: NF:webservices.WsReadBody
title: WsReadBody function (webservices.h)
description: This is a helper function that deserializes a value from the XML Readerof the message. The WS_MESSAGE_STATE must be set to WS_MESSAGE_STATE_READING. This function does not cause any state transitions.
helpviewer_keywords: ["WsReadBody","WsReadBody function [Web Services for Windows]","webservices/WsReadBody","wsw.wsreadbody"]
old-location: wsw\wsreadbody.htm
tech.root: wsw
ms.assetid: 43ceeb1e-aeb2-4482-90f0-d7f6013b239f
ms.date: 12/05/2018
ms.keywords: WsReadBody, WsReadBody function [Web Services for Windows], webservices/WsReadBody, wsw.wsreadbody
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
 - WsReadBody
 - webservices/WsReadBody
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
 - WsReadBody
---

# WsReadBody function


## -description

This is a helper function that deserializes a value from the XML Readerof the message.
            The <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE</a> must be set to <b>WS_MESSAGE_STATE_READING</b>.  This function does
                not cause any state transitions.

## -parameters

### -param message [in]

A pointer to the <b>Message</b> object to read the body from.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> object.

### -param bodyDescription [in]

A pointer to the object encapsulating the metadata that describes the mapping of the value to an element.

### -param readOption [in]

Determines whether the value is required and how to allocate the value.
                    See <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a> for more information.

### -param heap [in, optional]

A pointer to the <b>Heap</b> object to read the element into.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-heap">WS_HEAP</a> object.

### -param value

The interpretation of the data referenced by this parameter depends on the <b>WS_READ_OPTION</b>.

### -param valueSize [in]

The interpretation of the value of this parameter depends on the <b>WS_READ_OPTION</b>.

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
                of the <b>WS_ELEMENT_DESCRIPTION</b> supplied:
            

<ul>
<li>Reading a single element.  In this case, the elementLocalName and elementNs
                fields of the <b>WS_ELEMENT_DESCRIPTION</b> should be set to the local name
                and namespace of the element to read, and the type and type description represents
                the type of the value being deserialized.  If using <b>WS_FAULT_TYPE</b> or
                <b>WS_ENDPOINT_ADDRESS_TYPE</b> it is not necessary to specify the local name,
                namespace, or type description (they will default appropriately based on the
                envelope/addressing version of the message).
                </li>
<li>Reading multiple elements as a single value.  In this case, the elementLocalName and elementNs
                fields of the <b>WS_ELEMENT_DESCRIPTION</b> should be set to <b>NULL</b>, and a <b>WS_STRUCT_TYPE</b> and <a href="/windows/desktop/api/webservices/ns-webservices-ws_struct_description">WS_STRUCT_DESCRIPTION</a> should be specified.  In this case, each field of the
                structure value being deserialized should correspond to element(s) to read within the body.
                </li>
<li>Reading multiple elements as multiple values.  Reading multiple distinct values can be
                accomplished by simply calling the function multiple times.
            </li>
</ul>