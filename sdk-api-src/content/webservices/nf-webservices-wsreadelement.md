---
UID: NF:webservices.WsReadElement
title: WsReadElement function (webservices.h)
description: Read an element producing a value of the specified WS_TYPE.
helpviewer_keywords: ["WsReadElement","WsReadElement function [Web Services for Windows]","webservices/WsReadElement","wsw.wsreadelement"]
old-location: wsw\wsreadelement.htm
tech.root: wsw
ms.assetid: 88e0cc4d-ae24-46af-998d-fdbfbcc1be64
ms.date: 12/05/2018
ms.keywords: WsReadElement, WsReadElement function [Web Services for Windows], webservices/WsReadElement, wsw.wsreadelement
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
 - WsReadElement
 - webservices/WsReadElement
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
 - WsReadElement
---

# WsReadElement function


## -description

Read an element producing a value of the specified <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a>.

## -parameters

### -param reader [in]

The reader that is positioned on the XML to deserialize.

### -param elementDescription [in]

A pointer to a description of how to deserialize the element.

### -param readOption [in]

Whether the element is required, and how to allocate the value.  
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

This API will move to the next element, verify its name and namespace, and then
                and deserialize the content as a typed value.
            

If the API fails, the state of input reader becomes undefined. The only APIs that may be used on the reader
        if this occurs are <a href="/windows/desktop/api/webservices/nf-webservices-wssetinput">WsSetInput</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wssetinputtobuffer">WsSetInputToBuffer</a> to return the reader to a usable state,
        or <a href="/windows/desktop/api/webservices/nf-webservices-wsfreereader">WsFreeReader</a> to free the reader.