---
UID: NF:webservices.WsSetOutputToBuffer
title: WsSetOutputToBuffer function (webservices.h)
description: This operation positions the Writer at the end of the specified buffer.
helpviewer_keywords: ["WsSetOutputToBuffer","WsSetOutputToBuffer function [Web Services for Windows]","webservices/WsSetOutputToBuffer","wsw.wssetoutputtobuffer"]
old-location: wsw\wssetoutputtobuffer.htm
tech.root: wsw
ms.assetid: b969700d-7145-45eb-ad4b-c6e643975709
ms.date: 12/05/2018
ms.keywords: WsSetOutputToBuffer, WsSetOutputToBuffer function [Web Services for Windows], webservices/WsSetOutputToBuffer, wsw.wssetoutputtobuffer
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
 - WsSetOutputToBuffer
 - webservices/WsSetOutputToBuffer
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
 - WsSetOutputToBuffer
---

# WsSetOutputToBuffer function


## -description

This operation positions the Writer at the end of the specified buffer.
      
When an XML Writer has an XML Buffer set as output the Writer can be used in a "random access" fashion and the functions <a href="/windows/desktop/api/webservices/nf-webservices-wsgetwriterposition">WsGetWriterPosition</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wssetwriterposition">WsSetWriterPosition</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wsmovewriter">WsMoveWriter</a> can be used.

Properties specified for this function override those specified with the <code>WsCreateWriter</code> function. <div class="alert"><b>Note</b>  See <a href="/windows/desktop/api/webservices/nf-webservices-wscreatewriter">WsCreateWriter</a> for the default values of the properties of the writer.
</div>
<div> </div>

## -parameters

### -param writer [in]

A pointer to the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object for which the output is set.  The pointer must reference a valid <b>XML Writer</b> object.

### -param buffer [in]

A pointer to the buffer where the Writer sends the data.

### -param properties

A WS_XML_WRITER_PROPERTY pointer that  references an "array" of optional Writer properties.

### -param propertyCount [in]

The number of properties.

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
</table>

## -remarks

See <a href="/windows/desktop/api/webservices/nf-webservices-wscreatewriter">WsCreateWriter</a> for the default values of the properties of the writer.