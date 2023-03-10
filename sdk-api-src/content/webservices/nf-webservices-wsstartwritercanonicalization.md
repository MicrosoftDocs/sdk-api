---
UID: NF:webservices.WsStartWriterCanonicalization
title: WsStartWriterCanonicalization function (webservices.h)
description: Starts canonicalization on the specified XML writer.
helpviewer_keywords: ["WsStartWriterCanonicalization","WsStartWriterCanonicalization function [Web Services for Windows]","webservices/WsStartWriterCanonicalization","wsw.wsstartwritercanonicalization"]
old-location: wsw\wsstartwritercanonicalization.htm
tech.root: wsw
ms.assetid: e9ea26d6-a136-4103-ac67-42e943ea67b5
ms.date: 12/05/2018
ms.keywords: WsStartWriterCanonicalization, WsStartWriterCanonicalization function [Web Services for Windows], webservices/WsStartWriterCanonicalization, wsw.wsstartwritercanonicalization
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
 - WsStartWriterCanonicalization
 - webservices/WsStartWriterCanonicalization
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
 - WsStartWriterCanonicalization
---

# WsStartWriterCanonicalization function


## -description

Starts canonicalization on the specified XML writer.

## -parameters

### -param writer [in]

The XML writer on which canonicalization should be started.

### -param writeCallback [in]

The callback that to be invoked to write the canonical bytes as they are generated. This callback will always be invoked synchronously.

### -param writeCallbackState [in]

Caller-defined state that should be passed when invoking the <a href="/windows/desktop/api/webservices/nc-webservices-ws_write_callback">WS_WRITE_CALLBACK</a>.

### -param properties

An array of optional properties controlling how canonicalization is to be performed.  See <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_canonicalization_property">WS_XML_CANONICALIZATION_PROPERTY</a>.

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
</table>

## -remarks

The usage pattern for canonicalization is to:

<ul>
<li> call <b>WsStartWriterCanonicalization</b>,
</li>
<li> write the xml to be canonicalized,
</li>
<li> call <a href="/windows/desktop/api/webservices/nf-webservices-wsendwritercanonicalization">WsEndWriterCanonicalization</a>.
</li>
</ul>During this process, the canonical bytes will be written to the specified writeCallback.  Every node written by the writer will be canonicalized. Thus, canonicalization and generation can be done in one pass over regardless of what APIs are used to write the XML.
      
<a href="/windows/desktop/api/webservices/nf-webservices-wsendwritercanonicalization">WsEndWriterCanonicalization</a> must be called in order to ensure that all canonicalized bytes are written to the specified callback.

<a href="/windows/desktop/api/webservices/nf-webservices-wsendwritercanonicalization">WsEndWriterCanonicalization</a> must be called at the same depth at which <b>WsStartWriterCanonicalization</b> was called.  Other writer APIs will return an error if it would move to a depth lower than where <b>WsStartWriterCanonicalization</b> was called.
      
It is an invalid operation to call <a href="/windows/desktop/api/webservices/nf-webservices-wsmovewriter">WsMoveWriter</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wssetwriterposition">WsSetWriterPosition</a> on a writer between a pair of matching <b>WsStartWriterCanonicalization</b> and <a href="/windows/desktop/api/webservices/nf-webservices-wsendwritercanonicalization">WsEndWriterCanonicalization</a> calls.
      

Calls to this API cannot be nested.  So, a call to <b>WsStartWriterCanonicalization</b> must be followed by a call to <a href="/windows/desktop/api/webservices/nf-webservices-wsendwritercanonicalization">WsEndWriterCanonicalization</a> before the next <b>WsStartWriterCanonicalization</b> call.
      

If a <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_canonicalization_algorithm">WS_XML_CANONICALIZATION_ALGORITHM</a> is not specified, then <b>WS_EXCLUSIVE_XML_CANONICALIZATION_ALGORITHM</b> is used.
      

The <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_canonicalization_algorithm">WS_INCLUSIVE_XML_CANONICALIZATION_ALGORITHM</a> and <b>WS_INCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM</b> algorithms can only be used with entire xml documents.  The writer must positioned at <a href="/windows/desktop/api/webservices/ne-webservices-ws_xml_node_type">WS_XML_NODE_TYPE_BOF</a> when <b>WsStartWriterCanonicalization</b> is called with these algorithms.