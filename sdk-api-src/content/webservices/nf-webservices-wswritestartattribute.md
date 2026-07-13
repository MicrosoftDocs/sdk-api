---
UID: NF:webservices.WsWriteStartAttribute
title: WsWriteStartAttribute function (webservices.h)
description: This operation starts writing an attribute to the current element.
helpviewer_keywords: ["WsWriteStartAttribute","WsWriteStartAttribute function [Web Services for Windows]","webservices/WsWriteStartAttribute","wsw.wswritestartattribute"]
old-location: wsw\wswritestartattribute.htm
tech.root: wsw
ms.assetid: 9fd1eed9-6d8b-4b2e-a7ad-54a7f584734f
ms.date: 12/05/2018
ms.keywords: WsWriteStartAttribute, WsWriteStartAttribute function [Web Services for Windows], webservices/WsWriteStartAttribute, wsw.wswritestartattribute
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
 - WsWriteStartAttribute
 - webservices/WsWriteStartAttribute
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
 - WsWriteStartAttribute
---

# WsWriteStartAttribute function


## -description

This operation starts writing an attribute to the current element.
      <a href="/windows/desktop/api/webservices/nf-webservices-wswritestartelement">WsWriteStartElement</a> must be called before an attribute can be written.
      After the attribute has been started, the attribute value can be written
        using <a href="/windows/desktop/api/webservices/nf-webservices-wswritechars">WsWriteChars</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wswritebytes">WsWriteBytes</a>, or <a href="/windows/desktop/api/webservices/nf-webservices-wswritevalue">WsWriteValue</a>. The attribute must
        be completed using <a href="/windows/desktop/api/webservices/nf-webservices-wswriteendattribute">WsWriteEndAttribute</a>.

## -parameters

### -param writer [in]

A pointer to the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object to which the attribute is written.  The pointer must reference a valid <b>XML Writer</b> object.

### -param prefix [in, optional]

A WS_XML_STRING pointer to the prefix to use for the attribute.  If the value referenced by this parameter is <b>NULL</b> the Writer will choose a attribute.

### -param localName [in]

A WS_XML_STRING pointer to the local name used by the attribute.  It must be at least one character long.

### -param ns [in]

A WS_XML_STRING pointer to the namespace to be used for the attribute.
        
If no prefix is specified the Writer may use a prefix in scope that is bound to the specified namespace or it may generate a prefix and include an XMLNS attribute.

If a prefix is specified the Writer will use that prefix and may include an XMLNS attribute if needed to override an existing prefix in scope.

### -param singleQuote [in]

Determines whether to use a single or a double quote for the attribute value.

<div class="alert"><b>Note</b>  With <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_writer_binary_encoding">WS_XML_WRITER_BINARY_ENCODING</a> the quote character is not preserved and this parameter has no effect.
</div>
<div> </div>

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

If a <b>NULL</b> prefix is specified the writer will choose a prefix for the namespace.
      

To write an "xml:lang"  or "xml:space" attribute, specify "xml" for the prefix, "lang" or "space" for the localName,
        and "http://www.w3.org/XML/1998/namespace" for the namespace.
      

If writing the attribute causes <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_writer_property_id">WS_XML_WRITER_PROPERTY_MAX_ATTRIBUTES</a> to be exceeded
        then <b>WS_E_QUOTA_EXCEEDED</b> is returned.
      

If a non-empty prefix is specified with an empty namespace <b>WS_E_INVALID_FORMAT</b> is returned.
      (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)