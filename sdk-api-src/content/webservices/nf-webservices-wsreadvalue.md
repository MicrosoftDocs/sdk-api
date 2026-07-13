---
UID: NF:webservices.WsReadValue
title: WsReadValue function (webservices.h)
description: Reads text from a Reader and parses it according to the specified value type.
helpviewer_keywords: ["WsReadValue","WsReadValue function [Web Services for Windows]","webservices/WsReadValue","wsw.wsreadvalue"]
old-location: wsw\wsreadvalue.htm
tech.root: wsw
ms.assetid: d2dbeaf1-29cb-4848-8188-7922fdc15091
ms.date: 12/05/2018
ms.keywords: WsReadValue, WsReadValue function [Web Services for Windows], webservices/WsReadValue, wsw.wsreadvalue
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
 - WsReadValue
 - webservices/WsReadValue
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
 - WsReadValue
---

# WsReadValue function


## -description

Reads text from a Reader and parses it according to the specified value type.
      
The Reader reads from its current position up to the next Start or End element and parses them according to the specified value type.  If the Reader is already positioned on a Start or End element the buffer remains empty.
      
Comments are skipped and CDATA content is treated the same as other  element content.

Leading and trailing whitespaces are ignored. If the value cannot be parsed according to the specified value type, the function returns a <b>WS_E_INVALID_FORMAT</b> error code. (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)<div class="alert"><b>Note</b>  This function can fail for any of the reasons listed in <a href="/windows/desktop/api/webservices/nf-webservices-wsreadnode">WsReadNode</a>.
</div>
<div> </div>

## -parameters

### -param reader [in]

A pointer to the <b>XML Reader</b> from which the value is read.

### -param valueType [in]

The text interpretation type.

### -param value

A pointer to the parsed data if parsing was successful according to the specified value type.  The size required is determined by value type.  See <a href="/windows/desktop/api/webservices/ne-webservices-ws_value_type">WS_VALUE_TYPE</a> for more information.

### -param valueSize [in]

The byte size of the retrieved value.

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
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
A quota was exceeded.

</td>
</tr>
</table>

## -remarks

An example that reads an element containing an integer value.


``` syntax
// Advance the reader to the element
HRESULT hr = WsReadToStartElement(reader, localName, ns, NULL, error);
if (FAILED(hr))
{
    return hr;
}
// Advance past the element to the content
hr = WsReadStartElement(reader, error);
if (FAILED(hr))
{
    return hr;
}
// Read the content as an integer
__int32 i;
hr = WsReadValue(reader, WS_INT32_VALUE_TYPE, &i, sizeof(i), error);
if (FAILED(hr))
{
    return hr;
}
// Read the end element
hr = WsReadEndElement(reader, error);
if (FAILED(hr))
{
    return hr;
}
```

The grammar for the values types.


``` syntax

WS_BOOL_VALUE_TYPE     = "true"
                       | "false"
                       | "1"
                       | "0"
WS_INTxxx_VALUE_TYPE   = sign? digits
WS_UINTxxx_VALUE_TYPE  = digits
WS_FLOAT_VALUE_TYPE    = WS_DOUBLE_VALUE_TYPE
WS_DOUBLE_VALUE_TYPE   = sign? digits ("." digits)? exponent?
                       | "NaN"
                       | "INF"
                       | "-INF"
WS_DECIMAL_VALUE_TYPE  = sign? digits ("." digits)?
WS_GUID_VALUE_TYPE     = xxxxxxxx "-" xxxx "-" xxxx "-" xxxx "-" xxxxxxxxxxxx
WS_TIMESPAN_VALUE_TYPE = sign? (digits ".")? hh ":" mm ":" ss ("." d7)?
WS_DATETIME_VALUE_TYPE = yyyy "-" MM "-" dd "T" hh ":" mm ":" ss  ("." d7)? tz?
WS_DURATION_VALUE_TYPE = sign? "P" (digits "Y")  (digits "M")? (digits "D")?
                       | sign? "P" (digits "Y")? (digits "M")? (digits "D")?
                       | sign? "P" (digits "Y")? (digits "M")? (digits "D") 
                       | sign? "P" (digits "Y")? (digits "M")? (digits "D")? "T" (digits "H")  (digits "M")? (digits ("." digits)? "S")?
                       | sign? "P" (digits "Y")? (digits "M")? (digits "D")? "T" (digits "H")? (digits "M")  (digits ("." digits)? "S")?
                       | sign? "P" (digits "Y")? (digits "M")? (digits "D")? "T" (digits "H")? (digits "M")? (digits ("." digits)? "S")
sign                   = "-"
                       | "+"
exponent               = E sign? digits
                       | e sign? digits
digits                 = [0-9]+
x                      = [0-9]
                       | [A-F]
                       | [a-f]
yyyy                   = 1-9999
hh                     = 0-23
mm                     = 0-59
ss                     = 0-59
MM                     = 1-31
tz                     = "Z"
                       | sign hh ":" mm
d7                     = digit digit? digit? digit? digit? digit? digit?

```

