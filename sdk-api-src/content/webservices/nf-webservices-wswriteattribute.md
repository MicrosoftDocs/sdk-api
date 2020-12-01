---
UID: NF:webservices.WsWriteAttribute
title: WsWriteAttribute function (webservices.h)
description: Write a typed value as an XML attribute.
helpviewer_keywords: ["WsWriteAttribute","WsWriteAttribute function [Web Services for Windows]","webservices/WsWriteAttribute","wsw.wswriteattribute"]
old-location: wsw\wswriteattribute.htm
tech.root: wsw
ms.assetid: d1c02344-f5b9-4a59-b1c2-2dfb41df5ce1
ms.date: 12/05/2018
ms.keywords: WsWriteAttribute, WsWriteAttribute function [Web Services for Windows], webservices/WsWriteAttribute, wsw.wswriteattribute
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
 - WsWriteAttribute
 - webservices/WsWriteAttribute
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
 - WsWriteAttribute
---

# WsWriteAttribute function


## -description

Write a typed value as an XML attribute.

## -parameters

### -param writer [in]

The writer to write the attribute to.

### -param attributeDescription [in]

A pointer to a description of how to serialize the attribute.

### -param writeOption [in]

Information about how the value is allocated.
                    See <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_OPTION</a> for more information.

### -param value

A pointer to the value to serialize.

### -param valueSize [in]

The size of the value being serialized, in bytes.
                

If the value is <b>NULL</b>, then the size should be 0.

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
</table>

## -remarks

This API writes the start attribute, attribute value, and end attribute.
            

If the API fails, the state of input writer becomes undefined. The only APIs that may be used on the writer
        if this occurs are <a href="/windows/desktop/api/webservices/nf-webservices-wssetoutput">WsSetOutput</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wssetoutputtobuffer">WsSetOutputToBuffer</a> to return the writer to a usable state,
        or <a href="/windows/desktop/api/webservices/nf-webservices-wsfreewriter">WsFreeWriter</a> to free the writer.