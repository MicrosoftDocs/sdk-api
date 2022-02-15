---
UID: NF:webservices.WsReadEndElement
title: WsReadEndElement function (webservices.h)
description: This function ensures that the current Reader node is an End element and advances the reader to the next node.
helpviewer_keywords: ["WsReadEndElement","WsReadEndElement function [Web Services for Windows]","webservices/WsReadEndElement","wsw.wsreadendelement"]
old-location: wsw\wsreadendelement.htm
tech.root: wsw
ms.assetid: cd2e0e5a-9c73-4180-9c54-6742d87cb141
ms.date: 12/05/2018
ms.keywords: WsReadEndElement, WsReadEndElement function [Web Services for Windows], webservices/WsReadEndElement, wsw.wsreadendelement
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
 - WsReadEndElement
 - webservices/WsReadEndElement
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
 - WsReadEndElement
---

# WsReadEndElement function


## -description

This function ensures that the current Reader <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_node">node</a> is an <b>End element</b> and advances the reader to the next <b>node</b>.
      
If the Reader is not positioned on an <b>End element</b> when the function is called it will skip whitespace attempting to find one. If after skipping whitespace it is not positioned on an <b>End element</b> it returns a <b>WS_E_INVALID_FORMAT</b> exception.

(See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)

## -parameters

### -param reader [in]

A pointer to the <b>XML Reader</b> that is reads the <b>End element</b>. The pointer must reference a valid <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> object.

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

This function can fail for any of the reasons listed in <a href="/windows/desktop/api/webservices/nf-webservices-wsreadnode">WsReadNode</a>.