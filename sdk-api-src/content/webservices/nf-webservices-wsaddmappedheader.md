---
UID: NF:webservices.WsAddMappedHeader
title: WsAddMappedHeader function (webservices.h)
description: Adds a specified mapped header to the message.
helpviewer_keywords: ["WsAddMappedHeader","WsAddMappedHeader function [Web Services for Windows]","webservices/WsAddMappedHeader","wsw.wsaddmappedheader"]
old-location: wsw\wsaddmappedheader.htm
tech.root: wsw
ms.assetid: f91dac8e-606e-4a9f-a598-8f8136c6b386
ms.date: 12/05/2018
ms.keywords: WsAddMappedHeader, WsAddMappedHeader function [Web Services for Windows], webservices/WsAddMappedHeader, wsw.wsaddmappedheader
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
 - WsAddMappedHeader
 - webservices/WsAddMappedHeader
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
 - WsAddMappedHeader
---

# WsAddMappedHeader function


## -description

Adds a specified mapped header to the <a href="/windows/desktop/wsw/message">message</a>.

## -parameters

### -param message [in]

Pointer to a <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> structure representing the  <a href="/windows/desktop/wsw/message">message</a> to which to add the mapped header.
                

The message can be in any state except <b>WS_MESSAGE_STATE_EMPTY</b> (see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE</a> enumeration.

### -param headerName [in]

Pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_string">WS_XML_STRING</a> containing the name of the header.

### -param valueType [in]

The type of header value to deserialize.  For possible types and the corresponding headers, see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_header_type">WS_HEADER_TYPE</a>

### -param writeOption [in]

Whether the header is required, and how the value is allocated.
                    For more information, see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_OPTION</a> enumeration.

### -param value [in]

The header value to serialize.  For more information, see  the <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_OPTION</a> enumeration.

### -param valueSize [in]

The size of the value being serialized, in bytes.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

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
One or more of the parameters are incorrect.
                

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

A message may contain additional transport-specific information that is
                not part of the message envelope.  This transport-specific information
                can be exposed programmatically as headers of the message.
                The <b>WsAddMappedHeader</b> function is used to add such a header that will be mapped into some
                transport-specific location.
            

When you use the HTTP channel, you must specify the required mappings  before before you call this function to add the headers.  For more information, see <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_message_mapping">WS_HTTP_MESSAGE_MAPPING</a>.
            

If you are replacing a header, call the <a href="/windows/desktop/api/webservices/nf-webservices-wsremovemappedheader">WsRemoveMappedHeader</a> function to remove
                the existing instances of the header before you call <b>WsAddMappedHeader</b>.