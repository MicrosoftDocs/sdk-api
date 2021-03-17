---
UID: NF:webservices.WsReadChars
title: WsReadChars function (webservices.h)
description: Reads a specified number of text characters from the Reader.
helpviewer_keywords: ["WsReadChars","WsReadChars function [Web Services for Windows]","webservices/WsReadChars","wsw.wsreadchars"]
old-location: wsw\wsreadchars.htm
tech.root: wsw
ms.assetid: 3285d3f7-8ab1-42f0-b6e0-1d91aa0d576f
ms.date: 12/05/2018
ms.keywords: WsReadChars, WsReadChars function [Web Services for Windows], webservices/WsReadChars, wsw.wsreadchars
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
 - WsReadChars
 - webservices/WsReadChars
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
 - WsReadChars
---

# WsReadChars function


## -description

Reads a specified number of text characters from the Reader.

## -parameters

### -param reader [in]

A pointer to the <b>XML Reader</b> from which the character data should be read.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> object.

### -param chars

A pointer to a location for  the characters that have been read.

### -param maxCharCount [in]

The maximum number of characters that should be read.

### -param actualCharCount [out]

A pointer to a ULONG value of 
          the actual number of characters that were read.  This may be less than maxCharCount even when there
          are more characters remaining.  There are no more characters when this returns zero.

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

Text is read up to either a start element or end element.  Comments are skipped, and CDATA content is treated
        identically to element content.  Character entities are converted to their unescaped form.
      

This function can fail for any of the reasons listed in <a href="/windows/desktop/api/webservices/nf-webservices-wsreadnode">WsReadNode</a>.