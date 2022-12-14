---
UID: NF:webservices.WsFlushBody
title: WsFlushBody function (webservices.h)
description: Flushes all accumulated message body data that has been written.
helpviewer_keywords: ["WsFlushBody","WsFlushBody function [Web Services for Windows]","webservices/WsFlushBody","wsw.wsflushbody"]
old-location: wsw\wsflushbody.htm
tech.root: wsw
ms.assetid: f94c409b-94c0-4440-8587-74322777261f
ms.date: 12/05/2018
ms.keywords: WsFlushBody, WsFlushBody function [Web Services for Windows], webservices/WsFlushBody, wsw.wsflushbody
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
 - WsFlushBody
 - webservices/WsFlushBody
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
 - WsFlushBody
---

# WsFlushBody function


## -description

Flushes all accumulated message body data that has been written.
            

When message uses <a href="/windows/desktop/api/webservices/nf-webservices-wswritebody">WsWriteBody</a> or XML Writer, the data is accumulated in a buffer.   WsFlushBody subsequently performs the actual
                I/O.
            

WsFlushBody is typically used when  channel I/O is set to 
                <a href="/windows/desktop/api/webservices/ne-webservices-ws_transfer_mode">WS_STREAMED_OUTPUT_TRANSFER_MODE</a>, or when using an 
                XML Writer  set to use <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_stream_output">WS_XML_WRITER_STREAM_OUTPUT</a>.

## -parameters

### -param message [in]

A pointer to the <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> structure containing the accumulated message body data.

### -param minSize [in]

Specifies the minimum number of bytes that must be present in the
                    message for the function to perform the data flush.  
                

<div class="alert"><b>Note</b>  If the message contains less
                    than <i>minSize</i> WSFlushBody terminates without doing the I/O flush. A larger value will ensure that no I/O will be done until
                    the larger value has been accumulated.  This is useful for ensuring
                    that larger chunks are used when doing I/O.
                And presuming that 
                    there is at least one byte of accumulated data a value of 0 in  <i>minSize</i> guarantees that it will be flushed.
                </div>
<div> </div>

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
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>

## -remarks

This function is a "no-op" when <a href="/windows/desktop/api/webservices/ne-webservices-ws_transfer_mode">WS_STREAMED_OUTPUT_TRANSFER_MODE</a> is not set, or when using an
                XML Writer with <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_buffer_output">WS_XML_WRITER_BUFFER_OUTPUT</a> set.
      

This function is shortcut for calling <a href="/windows/desktop/api/webservices/nf-webservices-wsflushwriter">WsFlushWriter</a> for 
                the XML Writer being used to write the message.  Calling 
                <b>WsFlushWriter</b> directly is equivalent to calling this function.