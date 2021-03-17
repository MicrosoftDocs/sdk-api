---
UID: NF:webservices.WsWriteElement
title: WsWriteElement function (webservices.h)
description: Write a typed value as an XML element.
helpviewer_keywords: ["WsWriteElement","WsWriteElement function [Web Services for Windows]","webservices/WsWriteElement","wsw.wswriteelement"]
old-location: wsw\wswriteelement.htm
tech.root: wsw
ms.assetid: 5416d167-b832-4815-9826-6128f68dbc02
ms.date: 12/05/2018
ms.keywords: WsWriteElement, WsWriteElement function [Web Services for Windows], webservices/WsWriteElement, wsw.wswriteelement
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
 - WsWriteElement
 - webservices/WsWriteElement
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
 - WsWriteElement
---

# WsWriteElement function


## -description

Write a typed value as an XML element.

## -parameters

### -param writer [in]

The writer to write the element to.

### -param elementDescription [in]

A pointer to a description of how to serialize the element.

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

This API writes the start element, the attributes, child elements / text, and the end element
                that corresponds to the specified value.
            

If the API fails, the state of input writer becomes undefined. The only APIs that may be used on the writer
        if this occurs are <a href="/windows/desktop/api/webservices/nf-webservices-wssetoutput">WsSetOutput</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wssetoutputtobuffer">WsSetOutputToBuffer</a> to return the writer to a usable state,
        or <a href="/windows/desktop/api/webservices/nf-webservices-wsfreewriter">WsFreeWriter</a> to free the writer.