---
UID: NF:webservices.WsGetFaultErrorDetail
title: WsGetFaultErrorDetail function (webservices.h)
description: Read the fault detail stored in a WS_ERROR object.
helpviewer_keywords: ["WsGetFaultErrorDetail","WsGetFaultErrorDetail function [Web Services for Windows]","webservices/WsGetFaultErrorDetail","wsw.wsgetfaulterrordetail"]
old-location: wsw\wsgetfaulterrordetail.htm
tech.root: wsw
ms.assetid: 426c292f-64a5-411f-a63e-6be05fe93438
ms.date: 12/05/2018
ms.keywords: WsGetFaultErrorDetail, WsGetFaultErrorDetail function [Web Services for Windows], webservices/WsGetFaultErrorDetail, wsw.wsgetfaulterrordetail
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
 - WsGetFaultErrorDetail
 - webservices/WsGetFaultErrorDetail
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
 - WsGetFaultErrorDetail
---

# WsGetFaultErrorDetail function


## -description

Read the fault detail stored in a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object.

## -parameters

### -param error [in]

The error object that contains the fault information.

### -param faultDetailDescription [in]

A pointer to a description of the fault detail element.
                

The action value of the fault detail description is used as a filter
                    value to match against the action of the fault.  If both action
                    strings are specified (the action value of the fault detail description 
                    is not <b>NULL</b> and the action value <a href="/windows/desktop/api/webservices/ne-webservices-ws_fault_error_property_id">WS_FAULT_ERROR_PROPERTY_ACTION</a> in the 
                    <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> has a length greater than zero), then the action 
                    strings are compared to determine a match.  If there is a match, then the 
                    function will then try to deserialize the detail element.
                

The element description of the fault detail description is used to
                    describe the format of the element in the fault detail.

### -param readOption [in]

Whether the element is required, and how to allocate the value.
                    See <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a> for more information.

### -param heap [in, optional]

The heap to store the deserialized values in.

### -param value

The interpretation of this parameter depends on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a>.

### -param valueSize [in]

The interpretation of this parameter depends on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a>.

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
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The size quota of the heap was exceeded.
                

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
</table>

## -remarks

This API deserializes the value from the detail field of
                the <a href="/windows/desktop/api/webservices/ns-webservices-ws_fault">WS_FAULT</a> stored in the <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object.
            

This functions supports the following scenarios, based on the contents
                of the <a href="/windows/win32/api/webservices/ns-webservices-ws_fault_detail_description">WS_ELEMENT_DESCRIPTION</a> in the <a href="/windows/desktop/api/webservices/ns-webservices-ws_fault_detail_description">WS_FAULT_DETAIL_DESCRIPTION</a> supplied:
            

<ul>
<li>Reading a single element.  
                In this case, the elementLocalName and elementNs
                fields of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_element_description">WS_ELEMENT_DESCRIPTION</a> should be set to the local name
                and namespace of the element to read, and the type and type description represents
                the type of the value being deserialized.  
                

Since different faults with different detail formats may be expected
                from a service, this function can be called in succession to try to
                read each type of detail.  In this case, the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTIONAL_POINTER</a> value can be specified, which will return a <b>NULL</b> pointer if the element name
                in the fault detail does not match the expected value.
            

</li>
<li>Reading multiple elements as a single value.  
                In this case, the elementLocalName and elementNs
                fields of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_element_description">WS_ELEMENT_DESCRIPTION</a> should be set to <b>NULL</b>, and a <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_STRUCT_TYPE</a> and <a href="/windows/desktop/api/webservices/ns-webservices-ws_struct_description">WS_STRUCT_DESCRIPTION</a> should be specified.  Each field of the
                structure value being deserialized should correspond to element(s) to read within the body.
                The readOption parameter must be <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_REQUIRED_VALUE</a> or <b>WS_READ_REQUIRED_POINTER</b>. 
                

</li>
</ul>