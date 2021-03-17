---
UID: NF:webservices.WsReadNode
title: WsReadNode function (webservices.h)
description: This operation advances the Reader to the next node in the input stream.
helpviewer_keywords: ["WsReadNode","WsReadNode function [Web Services for Windows]","webservices/WsReadNode","wsw.wsreadnode"]
old-location: wsw\wsreadnode.htm
tech.root: wsw
ms.assetid: 60dacf3e-ebde-4247-be58-835565874ab6
ms.date: 12/05/2018
ms.keywords: WsReadNode, WsReadNode function [Web Services for Windows], webservices/WsReadNode, wsw.wsreadnode
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
 - WsReadNode
 - webservices/WsReadNode
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
 - WsReadNode
---

# WsReadNode function


## -description

This operation advances the Reader to the next <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_node">node</a> in the input stream.
      If there is an error parsing the input the function will return <b>WS_E_INVALID_FORMAT</b>.
      (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)

## -parameters

### -param reader [in]

A pointer to the <b>XML Reader</b> object to advance.
          The pointer must reference a valid <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> and it may not be <b>NULL</b>.

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
The input data was not in the expected format, or did not have the expected value, or multiple top-level elements were found and <b>WS_XML_READER_PROPERTY_ALLOW_FRAGMENT</b> is <b>FALSE</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
An element was read that exceeded some limit such as <b>WS_XML_READER_PROPERTY_MAX_DEPTH</b> or <b>WS_XML_READER_PROPERTY_MAX_ATTRIBUTES</b>.

</td>
</tr>
</table>

## -remarks

Other exception conditions include: <ul>
<li>If an XML declaration is found and <b>WS_XML_READER_PROPERTY_READ_DECLARATION</b> is <b>FALSE</b>,
        <b>WS_E_INVALID_FORMAT</b> is returned.
      </li>
<li>If the Reader is using <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_stream_input">WS_XML_READER_STREAM_INPUT</a> and there was insufficient data buffered the reader will return
        <b>WS_E_QUOTA_EXCEEDED</b>.
      </li>
</ul>