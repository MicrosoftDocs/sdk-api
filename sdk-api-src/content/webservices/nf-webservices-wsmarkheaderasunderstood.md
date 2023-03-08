---
UID: NF:webservices.WsMarkHeaderAsUnderstood
title: WsMarkHeaderAsUnderstood function (webservices.h)
description: This function marks a header as &quot;understood&quot; by the application.
helpviewer_keywords: ["WsMarkHeaderAsUnderstood","WsMarkHeaderAsUnderstood function [Web Services for Windows]","webservices/WsMarkHeaderAsUnderstood","wsw.wsmarkheaderasunderstood"]
old-location: wsw\wsmarkheaderasunderstood.htm
tech.root: wsw
ms.assetid: f119f85a-f6a7-4472-8177-a2e23b6d12f9
ms.date: 12/05/2018
ms.keywords: WsMarkHeaderAsUnderstood, WsMarkHeaderAsUnderstood function [Web Services for Windows], webservices/WsMarkHeaderAsUnderstood, wsw.wsmarkheaderasunderstood
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
 - WsMarkHeaderAsUnderstood
 - webservices/WsMarkHeaderAsUnderstood
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
 - WsMarkHeaderAsUnderstood
---

# WsMarkHeaderAsUnderstood function


## -description

This function marks a header as "understood" by the application.
            
The set of headers is extensible and Message assimilation by the receiver is not accessible by the sender.  This function is the receiving applications method for making it known to the sender that the received header has been read and understood.
<div class="alert"><b>Note</b>  This function should be used only if the application receives a message indicating that the  header must be understood and it did not acquire the header using <a href="/windows/desktop/api/webservices/nf-webservices-wsgetheader">WsGetHeader</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsgetcustomheader">WsGetCustomHeader</a>.

The <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE</a> must be in the set to  <b>WS_MESSAGE_STATE_READING</b>. See .<a href="/windows/desktop/api/webservices/nf-webservices-wscheckmustunderstandheaders">WsCheckMustUnderstandHeaders</a> for more information.</div><div> </div>

## -parameters

### -param message [in]

A pointer to the Message object with the header to mark.

### -param headerPosition [in]

A pointer to the position of the header element within the XML header segment.

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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The message is not in the correct state.
                

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

When the application reads the header using an XML Reader,
                it should obtain a <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_node_position">WS_XML_NODE_POSITION</a> of the header element
                and pass it to this function.  See <a href="/windows/desktop/api/webservices/nf-webservices-wsgetreaderposition">WsGetReaderPosition</a> for
                how to obtain a <b>WS_XML_NODE_POSITION</b>.