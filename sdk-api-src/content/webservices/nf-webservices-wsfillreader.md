---
UID: NF:webservices.WsFillReader
title: WsFillReader function (webservices.h)
description: Ensures that the reader has buffered the minimum byte count of XML data for use by subsequent reader functions.
helpviewer_keywords: ["WsFillReader","WsFillReader function [Web Services for Windows]","webservices/WsFillReader","wsw.wsfillreader"]
old-location: wsw\wsfillreader.htm
tech.root: wsw
ms.assetid: 1f4138a2-acc5-4f1d-8e35-544859d2fa49
ms.date: 12/05/2018
ms.keywords: WsFillReader, WsFillReader function [Web Services for Windows], webservices/WsFillReader, wsw.wsfillreader
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
 - WsFillReader
 - webservices/WsFillReader
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
 - WsFillReader
---

# WsFillReader function


## -description

Ensures that the reader has buffered the minimum byte count of XML data for use by subsequent reader functions.  It will invoke the callback specified by <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_stream_input">WS_XML_READER_STREAM_INPUT</a> as many times as necessary to obtain the number of bytes specified by the value of the <i>minSize</i> parameter.  On completion the buffered data is available to other reader functions.  If a subsequent reader function requires more data than what has been obtained the function
        will return a <b>WS_E_QUOTA_EXCEEDED</b> exception.
      (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)

## -parameters

### -param reader [in]

A  pointer to a <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> structure used for obtaining the data.

### -param minSize [in]

Specifies the minimum number of bytes that the reader should have obtained.  If the current byte count buffered is equal to or greater than the value of <i>minSize</i> the function will do nothing and will return immediately.

### -param asyncContext [in, optional]

A pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_async_context">WS_ASYNC_CONTEXT</a> data structure with information about invoking the function asynchronously.  A <b>NULL</b> 
                 value indicates a request for synchronous operation.

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
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation is still pending.
        

</td>
</tr>
</table>

## -remarks

The number of bytes required to read a particular segment of XML data depends upon the encoding
        and its formatting.
      

This function is a "no-op" when used with a reader using <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_buffer_input">WS_XML_READER_BUFFER_INPUT</a>.
      

By specifying a <a href="/windows/desktop/api/webservices/ns-webservices-ws_async_context">WS_ASYNC_CONTEXT</a> the data is read asynchronously.