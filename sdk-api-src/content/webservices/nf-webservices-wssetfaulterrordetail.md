---
UID: NF:webservices.WsSetFaultErrorDetail
title: WsSetFaultErrorDetail function (webservices.h)
description: Write the fault detail stored in a WS_ERROR object.
helpviewer_keywords: ["WsSetFaultErrorDetail","WsSetFaultErrorDetail function [Web Services for Windows]","webservices/WsSetFaultErrorDetail","wsw.wssetfaulterrordetail"]
old-location: wsw\wssetfaulterrordetail.htm
tech.root: wsw
ms.assetid: 469982a5-42da-40e7-a053-4820fee58828
ms.date: 12/05/2018
ms.keywords: WsSetFaultErrorDetail, WsSetFaultErrorDetail function [Web Services for Windows], webservices/WsSetFaultErrorDetail, wsw.wssetfaulterrordetail
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
 - WsSetFaultErrorDetail
 - webservices/WsSetFaultErrorDetail
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
 - WsSetFaultErrorDetail
---

# WsSetFaultErrorDetail function


## -description

Write the fault detail stored in a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object.

## -parameters

### -param error [in]

The error object that will contain the fault information.

### -param faultDetailDescription [in]

A pointer to a description of the fault detail.
                

If the action field of the fault detail description is non-<b>NULL</b>,
                    then it is set as the <a href="/windows/desktop/api/webservices/ne-webservices-ws_fault_error_property_id">WS_FAULT_ERROR_PROPERTY_ACTION</a> of the <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a>.
                

The element description of the fault detail description 
                    describes the format of the element in the fault detail.

### -param writeOption [in]

Information about how the value is allocated.
                    See <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_OPTION</a> for more information.

### -param value

A pointer to the value to serialize.

### -param valueSize [in]

The size of the value being serialized, in bytes.
                

If the value is <b>NULL</b>, then the size should be 0.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
</table>

## -remarks

This API will serialize the value of the detail field of
                the <a href="/windows/desktop/api/webservices/ns-webservices-ws_fault">WS_FAULT</a> stored in the <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object.
            

This functions supports the following scenarios, based on the contents
                of the <a href="/windows/win32/api/webservices/ns-webservices-ws_fault_detail_description">WS_ELEMENT_DESCRIPTION</a> in the <a href="/windows/desktop/api/webservices/ns-webservices-ws_fault_detail_description">WS_FAULT_DETAIL_DESCRIPTION</a> supplied:
            

<ul>
<li>Writing a single element.  In this case, the elementLocalName and elementNs
                fields of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_element_description">WS_ELEMENT_DESCRIPTION</a> should be set to the local name
                and namespace of the element to write, and the type and type description represents
                the type of the value being serialized.  
                </li>
<li>Writing multiple elements as a single value.  In this case, the elementLocalName and elementNs
                fields of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_element_description">WS_ELEMENT_DESCRIPTION</a> should be set to <b>NULL</b>, and a <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_STRUCT_TYPE</a> and <a href="/windows/desktop/api/webservices/ns-webservices-ws_struct_description">WS_STRUCT_DESCRIPTION</a> should be specified.  Each field of the
                structure value being serialized should correspond to element(s) to write within the fault detail.
                The writeOption parameter must be either <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_REQUIRED_VALUE</a> or 
                <b>WS_WRITE_REQUIRED_POINTER</b>.                
                </li>
</ul>