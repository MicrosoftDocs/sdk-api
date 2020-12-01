---
UID: NF:webservices.WsReadAttribute
title: WsReadAttribute function (webservices.h)
description: Read an attribute producing a value of the specified WS_TYPE.
helpviewer_keywords: ["WsReadAttribute","WsReadAttribute function [Web Services for Windows]","webservices/WsReadAttribute","wsw.wsreadattribute"]
old-location: wsw\wsreadattribute.htm
tech.root: wsw
ms.assetid: 2055182a-8aff-4db0-88f1-d344ca89e383
ms.date: 12/05/2018
ms.keywords: WsReadAttribute, WsReadAttribute function [Web Services for Windows], webservices/WsReadAttribute, wsw.wsreadattribute
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
 - WsReadAttribute
 - webservices/WsReadAttribute
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
 - WsReadAttribute
---

# WsReadAttribute function


## -description

Read an attribute producing a value of the specified <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a>.

## -parameters

### -param reader [in]

The reader that is positioned on the element containing the attribute.

### -param attributeDescription [in]

A pointer to a description of how to deserialize the attribute.

### -param readOption [in]

Whether the attribute is required, and how to allocate the value.
                    See <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a> for more information.

### -param heap [in, optional]

The heap to store the deserialized values in.

### -param value

The interpretation of this parameter depends on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a>.

### -param valueSize [in]

The interpretation of this parameter depends on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a>.

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

This API will search for the attribute given the name and namespace, and then
                and deserialize the content as a typed value.
            

If the API fails, the state of input reader becomes undefined. The only APIs that may be used on the reader
        if this occurs are <a href="/windows/desktop/api/webservices/nf-webservices-wssetinput">WsSetInput</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wssetinputtobuffer">WsSetInputToBuffer</a> to return the reader to a usable state,
        or <a href="/windows/desktop/api/webservices/nf-webservices-wsfreereader">WsFreeReader</a> to free the reader.