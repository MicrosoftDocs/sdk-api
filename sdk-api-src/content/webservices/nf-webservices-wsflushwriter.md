---
UID: NF:webservices.WsFlushWriter
title: WsFlushWriter function (webservices.h)
description: Instructs the writer to invoke the callbackspecified in WS_XML_WRITER_STREAM_OUTPUT if sufficient data has been buffered.
helpviewer_keywords: ["WsFlushWriter","WsFlushWriter function [Web Services for Windows]","webservices/WsFlushWriter","wsw.wsflushwriter"]
old-location: wsw\wsflushwriter.htm
tech.root: wsw
ms.assetid: ba631942-d5a0-4d93-9899-c3f0ebd4aae5
ms.date: 12/05/2018
ms.keywords: WsFlushWriter, WsFlushWriter function [Web Services for Windows], webservices/WsFlushWriter, wsw.wsflushwriter
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
 - WsFlushWriter
 - webservices/WsFlushWriter
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
 - WsFlushWriter
---

# WsFlushWriter function


## -description

Instructs the writer to invoke the <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_stream_output">callback</a> specified in <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_stream_output">WS_XML_WRITER_STREAM_OUTPUT</a> if sufficient data has been buffered.

## -parameters

### -param writer [in]

The writer to flush.

### -param minSize [in]

Specifies the minimum number of bytes that must be buffered in order for the
          <a href="/windows/desktop/api/webservices/nc-webservices-ws_write_callback">callback</a> to be invoked. If fewer than this number of bytes
          are buffered, then the <b>callback</b> will not be invoked.  This can be
          used to minimize the number of i/o's that occur when writing small amounts of data.
        

Zero should be specified to guarantee that the <a href="/windows/desktop/api/webservices/nc-webservices-ws_write_callback">callback</a> is invoked.

### -param asyncContext [in, optional]

Information on how to invoke the function asynchronously, or <b>NULL</b> if invoking synchronously.

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
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation is still pending.
        

</td>
</tr>
</table>

## -remarks

The writer buffers all data until <b>WsFlushWriter</b> is called.
      

If necessary, the <b>WsFlushWriter</b> should be called before <a href="/windows/desktop/api/webservices/nf-webservices-wsfreewriter">WsFreeWriter</a> to guarantee all data is emitted.
      

By specifying a <a href="/windows/desktop/api/webservices/ns-webservices-ws_async_context">WS_ASYNC_CONTEXT</a> the buffered data will be written asynchronously.
      

This function is a no-op if the writer is using <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_buffer_output">WS_XML_WRITER_BUFFER_OUTPUT</a>.
      

If <a href="/windows/desktop/api/webservices/nf-webservices-wswritestartelement">WsWriteStartElement</a> has been called, but the element has not been committed (see <b>WsWriteStartElement</b>)
        then this element will not be flushed.
      

If this function is called when using <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_mtom_encoding">WS_XML_WRITER_MTOM_ENCODING</a> and there are
        no open elements on the writer, then the supporting MIME parts will be generated and emitted.  Once this
        occurs, any API that attempts to write further to the XML document will return <b>WS_E_INVALID_OPERATION</b>.
      (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)