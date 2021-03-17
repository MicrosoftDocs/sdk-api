---
UID: NF:webservices.WsWriteType
title: WsWriteType function (webservices.h)
description: Write a value of a given WS_TYPE to XML according to the WS_TYPE_MAPPING.
helpviewer_keywords: ["WsWriteType","WsWriteType function [Web Services for Windows]","webservices/WsWriteType","wsw.wswritetype"]
old-location: wsw\wswritetype.htm
tech.root: wsw
ms.assetid: cab1b4d6-c18b-4740-b4a4-61e70ea181d9
ms.date: 12/05/2018
ms.keywords: WsWriteType, WsWriteType function [Web Services for Windows], webservices/WsWriteType, wsw.wswritetype
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
 - WsWriteType
 - webservices/WsWriteType
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
 - WsWriteType
---

# WsWriteType function


## -description

Write a value of a given <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a> to XML according to the <a href="/windows/desktop/api/webservices/ne-webservices-ws_type_mapping">WS_TYPE_MAPPING</a>.

## -parameters

### -param writer [in]

The writer to write the value to.

### -param typeMapping [in]

Describes how the type maps to the XML that is being written.

### -param type [in]

The type of the value to serialize.

### -param typeDescription [in, optional]

Additional information about the type.  Each type has a different description
                    structure.  This may be <b>NULL</b>, depending on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a>.

### -param writeOption [in]

Whether the value is required, and how the value is allocated.
                    See <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_OPTION</a> for more information.
                

This parameter must have one of the following values:
                

<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_REQUIRED_VALUE</a>.
                    </li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_REQUIRED_POINTER</a>.
                </li>
</ul>

### -param value

A pointer to the value to serialize.

### -param valueSize [in]

The size of the value being serialized.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

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

See <a href="/windows/desktop/api/webservices/ne-webservices-ws_type_mapping">WS_TYPE_MAPPING</a> for how to use this function to write values in elements and attributes.                
            

If the API fails, the state of input writer becomes undefined. The only APIs that may be used on the writer
        if this occurs are <a href="/windows/desktop/api/webservices/nf-webservices-wssetoutput">WsSetOutput</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wssetoutputtobuffer">WsSetOutputToBuffer</a> to return the writer to a usable state,
        or <a href="/windows/desktop/api/webservices/nf-webservices-wsfreewriter">WsFreeWriter</a> to free the writer.