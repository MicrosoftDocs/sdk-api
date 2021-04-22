---
UID: NF:webservices.WsSetReaderPosition
title: WsSetReaderPosition function (webservices.h)
description: Sets the current position of the Reader. The position must have been obtained by a call to WsGetReaderPosition or WsGetWriterPosition. This function can only be used on a reader that is set to a WS_XML_BUFFER.
helpviewer_keywords: ["WsSetReaderPosition","WsSetReaderPosition function [Web Services for Windows]","webservices/WsSetReaderPosition","wsw.wssetreaderposition"]
old-location: wsw\wssetreaderposition.htm
tech.root: wsw
ms.assetid: cc879cc0-c8ca-457e-9ff1-ae220e31cb04
ms.date: 12/05/2018
ms.keywords: WsSetReaderPosition, WsSetReaderPosition function [Web Services for Windows], webservices/WsSetReaderPosition, wsw.wssetreaderposition
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
 - WsSetReaderPosition
 - webservices/WsSetReaderPosition
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
 - WsSetReaderPosition
---

# WsSetReaderPosition function


## -description

Sets the current position of the Reader.  The position must have been obtained by a call to <a href="/windows/desktop/api/webservices/nf-webservices-wsgetreaderposition">WsGetReaderPosition</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsgetwriterposition">WsGetWriterPosition</a>.
      
This function can only be used on a reader that is set to a <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a>.

## -parameters

### -param reader [in]

A pointer to the <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> object for which the current position is set.  The pointer must reference a valid <b>XML Reader</b> object.

### -param nodePosition [in]

A pointer to the position to set the Reader.

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
</table>

## -remarks

See <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_node_position">WS_XML_NODE_POSITION</a> for more information on using positions.
      

This function cannot be used while canonicalizing.  If <a href="/windows/desktop/api/webservices/nf-webservices-wsstartreadercanonicalization">WsStartReaderCanonicalization</a> has
        been called, then it will return <b>WS_E_INVALID_OPERATION</b>.
      (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)