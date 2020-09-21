---
UID: NF:webservices.WsSetOutput
title: WsSetOutput function (webservices.h)
description: Sets the encoding and output callbacks for the writer. The callbacks are used to provides buffers to the writer and to perform asynchronous i/o.
helpviewer_keywords: ["WsSetOutput","WsSetOutput function [Web Services for Windows]","webservices/WsSetOutput","wsw.wssetoutput"]
old-location: wsw\wssetoutput.htm
tech.root: wsw
ms.assetid: f0b47817-0ad1-408c-a6da-9a7b0fb2e34b
ms.date: 12/05/2018
ms.keywords: WsSetOutput, WsSetOutput function [Web Services for Windows], webservices/WsSetOutput, wsw.wssetoutput
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
 - WsSetOutput
 - webservices/WsSetOutput
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
 - WsSetOutput
---

# WsSetOutput function


## -description

Sets the encoding and output callbacks for the writer.  The callbacks are used to 
        provides buffers to the writer and to perform asynchronous i/o.

## -parameters

### -param writer [in]

The writer for which the output will be set.

### -param encoding [in, optional]

The encoding describes the format of the input bytes.  This should be one of <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_text_encoding">WS_XML_WRITER_TEXT_ENCODING</a>,
          <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_binary_encoding">WS_XML_WRITER_BINARY_ENCODING</a> or <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_mtom_encoding">WS_XML_WRITER_MTOM_ENCODING</a>.

### -param output [in, optional]

Specifies where the writer should place its data.

### -param properties

An array of optional properties of the writer.  See <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_property">WS_XML_WRITER_PROPERTY</a>.

### -param propertyCount [in]

The number of properties.

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
</table>

## -remarks

When <b>WsSetOutput</b> is used on the writer, the writer will function in a forward only manner and
        the functions <a href="/windows/desktop/api/webservices/nf-webservices-wsgetwriterposition">WsGetWriterPosition</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wssetwriterposition">WsSetWriterPosition</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wsmovewriter">WsMoveWriter</a> cannot be used.
      

If <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_encoding">encoding</a> is <b>NULL</b>, then <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_output">WS_XML_WRITER_OUTPUT</a> is ignored and the writer is set up so that any attempt to write to it will fail.
      

If <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_encoding">encoding</a> is not <b>NULL</b>, then <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_output">WS_XML_WRITER_OUTPUT</a> must be non-<b>NULL</b> as well.
      

If <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_buffer_output">WS_XML_WRITER_OUTPUT</a> is <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_buffer_output">WS_XML_WRITER_BUFFER_OUTPUT</a> then the writer will buffer the generated
        bytes of the document.  Use <a href="/windows/desktop/api/webservices/nf-webservices-wsgetwriterproperty">WsGetWriterProperty</a> with <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_writer_property_id">WS_XML_WRITER_PROPERTY_BUFFERS</a> or
        <b>WS_XML_WRITER_PROPERTY_BYTES</b> to obtain these bytes.  In this mode <a href="/windows/desktop/api/webservices/nf-webservices-wsflushwriter">WsFlushWriter</a> has no effect.
      

If <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_stream_output">WS_XML_WRITER_OUTPUT</a> is <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_stream_output">WS_XML_WRITER_STREAM_OUTPUT</a> then the writer will pass the generated
        bytes of the document to the specified <a href="/windows/desktop/api/webservices/nc-webservices-ws_write_callback">WS_WRITE_CALLBACK</a> during calls to <a href="/windows/desktop/api/webservices/nf-webservices-wsflushwriter">WsFlushWriter</a>.
      

The writer will be initialized to use the properties specified in <a href="/windows/desktop/api/webservices/nf-webservices-wscreatewriter">WsCreateWriter</a>.  Any properties
        specified to <b>WsSetOutput</b> will override those properties.
      

See <a href="/windows/desktop/api/webservices/nf-webservices-wscreatewriter">WsCreateWriter</a> for the default values of the properties of the writer.