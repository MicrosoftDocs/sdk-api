---
UID: NF:webservices.WsReadArray
title: WsReadArray function (webservices.h)
description: Reads a series of elements from the reader and interprets their content according to the specified value type.
helpviewer_keywords: ["WsReadArray","WsReadArray function [Web Services for Windows]","webservices/WsReadArray","wsw.wsreadarray"]
old-location: wsw\wsreadarray.htm
tech.root: wsw
ms.assetid: ab545d74-7a61-48db-8c84-11017ee65605
ms.date: 12/05/2018
ms.keywords: WsReadArray, WsReadArray function [Web Services for Windows], webservices/WsReadArray, wsw.wsreadarray
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
 - WsReadArray
 - webservices/WsReadArray
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
 - WsReadArray
---

# WsReadArray function


## -description

Reads a series of elements from the reader and interprets their 
        content according to the specified value type.

## -parameters

### -param reader [in]

The reader from which the array should be read.

### -param localName [in]

The localName of the repeating element.

### -param ns [in]

The namespace of the repeating element.

### -param valueType [in]

The value type to use to parse the content of each element.

### -param array

The array to populate with parsed values.  The size of the array items is determined by the value type.
          See <a href="/windows/desktop/api/webservices/ne-webservices-ws_value_type">WS_VALUE_TYPE</a> for more information.

### -param arraySize [in]

The size in bytes (not items) of the array.

### -param itemOffset [in]

The item (not byte) offset within the array at which to read.

### -param itemCount [in]

The number of items (not bytes) to read into the array.

### -param actualItemCount [out]

The actual number of items that were read.  This may be less than itemCount even when there
          are more items remaining.  There are no more elements when this returns zero.

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
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
A quota was exceeded.

</td>
</tr>
</table>

## -remarks

This function is semantically equivalent to using <a href="/windows/desktop/api/webservices/nf-webservices-wsreadstartelement">WsReadStartElement</a>,
        <a href="/windows/desktop/api/webservices/nf-webservices-wsreadvalue">WsReadValue</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wsreadendelement">WsReadEndElement</a> in a loop, but is more efficient.
      

This function can fail for any of the reasons listed in <a href="/windows/desktop/api/webservices/nf-webservices-wsreadnode">WsReadNode</a>.