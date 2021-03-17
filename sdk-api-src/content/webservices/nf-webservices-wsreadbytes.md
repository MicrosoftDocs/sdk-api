---
UID: NF:webservices.WsReadBytes
title: WsReadBytes function (webservices.h)
description: Reads text from the Reader and decodes the characters as bytes according to the base64 specification.
helpviewer_keywords: ["WsReadBytes","WsReadBytes function [Web Services for Windows]","webservices/WsReadBytes","wsw.wsreadbytes"]
old-location: wsw\wsreadbytes.htm
tech.root: wsw
ms.assetid: 02cff29c-7d39-4df2-8eb1-506f93959a1e
ms.date: 12/05/2018
ms.keywords: WsReadBytes, WsReadBytes function [Web Services for Windows], webservices/WsReadBytes, wsw.wsreadbytes
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
 - WsReadBytes
 - webservices/WsReadBytes
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
 - WsReadBytes
---

# WsReadBytes function


## -description

Reads text from the Reader and decodes the characters as bytes according to the base64 specification.

## -parameters

### -param reader [in]

A pointer to the <b>XML Reader</b> from which the bytes should be read.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> object.

### -param bytes

A pointer to a location to place the decoded bytes.

### -param maxByteCount [in]

The maximum number of bytes that should be read.

### -param actualByteCount [out]

A pointer to a ULONG value of 
          the actual number of bytes that were read.  This may be less than maxByteCount even when there
          are more bytes remaining.

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
        identically to element content.
      

This function can fail for any of the reasons listed in <a href="/windows/desktop/api/webservices/nf-webservices-wsreadnode">WsReadNode</a>.