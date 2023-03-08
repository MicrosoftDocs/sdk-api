---
UID: NF:webservices.WsCreateWriter
title: WsCreateWriter function (webservices.h)
description: creates an XML Writer with the specified properties.
helpviewer_keywords: ["WsCreateWriter","WsCreateWriter function [Web Services for Windows]","webservices/WsCreateWriter","wsw.wscreatewriter"]
old-location: wsw\wscreatewriter.htm
tech.root: wsw
ms.assetid: 5b4bb009-764e-4892-903a-5939f5570016
ms.date: 12/05/2018
ms.keywords: WsCreateWriter, WsCreateWriter function [Web Services for Windows], webservices/WsCreateWriter, wsw.wscreatewriter
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
 - WsCreateWriter
 - webservices/WsCreateWriter
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
 - WsCreateWriter
---

# WsCreateWriter function


## -description

creates an <a href="/windows/desktop/wsw/xml-writer">XML Writer</a> with the specified properties.

## -parameters

### -param properties

An array of <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_writer_property">WS_XML_WRITER_PROPERTY</a> structures containing optional properties for the XML writer.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).

### -param propertyCount [in]

The number of properties in the <i>properties</i> array.

### -param writer

On   success, a pointer that receives the address of the  <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> structure representing the created XML writer.
                
When you no longer need this structure, you must free it by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsfreewriter">WsFreeWriter</a>.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

## -returns

If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

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

Use the <a href="/windows/desktop/api/webservices/nf-webservices-wssetoutput">WsSetOutput</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wssetoutputtobuffer">WsSetOutputToBuffer</a> functions to choose the encoding of the XML writer and to indicate where to direct the output.
      

A <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> can be reused by calling <a href="/windows/desktop/api/webservices/nf-webservices-wssetoutput">WsSetOutput</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wssetoutputtobuffer">WsSetOutputToBuffer</a> again.
      

See <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_writer_property_id">WS_XML_WRITER_PROPERTY_ID</a> for the properties that can be used to configure the writer.
      

The XML writer buffers all data until <a href="/windows/desktop/api/webservices/nf-webservices-wsflushwriter">WsFlushWriter</a> is called.  This allows the caller to determine at what granularity to write data and to whether to write that data asynchronously.  Data is not written until <b>WsFlushWriter</b> is called.
      

If an operation on a  <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> fails the writer is left in a faulted state and further calls to the Writer return <b>WS_E_OBJECT_FAULTED</b>.  (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)The only possible function calls for the XML writer if this occurs are <a href="/windows/desktop/api/webservices/nf-webservices-wssetoutput">WsSetOutput</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wssetoutputtobuffer">WsSetOutputToBuffer</a> to return the XML writer to a usable state, or <a href="/windows/desktop/api/webservices/nf-webservices-wsfreewriter">WsFreeWriter</a> to free the XML writer.