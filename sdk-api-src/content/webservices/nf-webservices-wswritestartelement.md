---
UID: NF:webservices.WsWriteStartElement
title: WsWriteStartElement function (webservices.h)
description: Writes a start element to the writer.
helpviewer_keywords: ["WsWriteStartElement","WsWriteStartElement function [Web Services for Windows]","webservices/WsWriteStartElement","wsw.wswritestartelement"]
old-location: wsw\wswritestartelement.htm
tech.root: wsw
ms.assetid: da23f5e6-504c-4e93-9190-7d8c41efc0da
ms.date: 12/05/2018
ms.keywords: WsWriteStartElement, WsWriteStartElement function [Web Services for Windows], webservices/WsWriteStartElement, wsw.wswritestartelement
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
 - WsWriteStartElement
 - webservices/WsWriteStartElement
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
 - WsWriteStartElement
---

# WsWriteStartElement function


## -description

Writes a start element to the writer.
      

After calling this function <a href="/windows/desktop/api/webservices/nf-webservices-wswritestartattribute">WsWriteStartAttribute</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wswritexmlnsattribute">WsWriteXmlnsAttribute</a> can be called to write additional attributes to the element. The element is not committed to the writer until <a href="/windows/desktop/api/webservices/nf-webservices-wswriteendelement">WsWriteEndElement</a> or some other function  that  writes content is called.

## -parameters

### -param writer [in]

A pointer to the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object to which the start element is written.  The pointer must reference a valid <b>XML Writer</b> object.

### -param prefix [in, optional]

A WS_XML_STRING pointer to the prefix to use for the start element.  If the value referenced by this parameter is <b>NULL</b> the Writer will choose a attribute.

### -param localName [in]

A WS_XML_STRING pointer to the local name used by the start element.  It must be at least one character long.

### -param ns [in]

A WS_XML_STRING pointer to the namespace to be used for the start element.
        
If no prefix is specified the Writer may use a prefix in scope that is bound to the specified namespace or it may generate a prefix and include an XMLNS attribute. If a prefix is specified the Writer will use that prefix and may include an XMLNS attribute if needed to override an existing prefix in scope.

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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed due to the current state of the object.

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
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
A quota was exceeded.

</td>
</tr>
</table>

## -remarks

If the underlying encoding supports empty elements and the element has no content an empty element is written.
      

If a non-empty prefix is specified with an empty namespace <b>WS_E_INVALID_FORMAT</b> is returned.
      

If writing the start element causes <b>WS_XML_WRITER_PROPERTY_MAX_DEPTH</b> to be exceeded
        <b>WS_E_QUOTA_EXCEEDED</b> is returned.
       (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)

When using <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_mtom_encoding">WS_XML_WRITER_MTOM_ENCODING</a> it is an error to attempt to write an element with the
        localName "Include" from the namespace"http://www.w3.org/2004/08/xop/include".
      


<a href="/windows/desktop/api/webservices/nf-webservices-wswritestartattribute">WsWriteStartAttribute</a> can also be used to add an attribute to an element when the writer is
        positioned on an element using <a href="/windows/desktop/api/webservices/nf-webservices-wsmovewriter">WsMoveWriter</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wssetwriterposition">WsSetWriterPosition</a>.