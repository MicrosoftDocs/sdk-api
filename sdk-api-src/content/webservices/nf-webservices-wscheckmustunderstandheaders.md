---
UID: NF:webservices.WsCheckMustUnderstandHeaders
title: WsCheckMustUnderstandHeaders function (webservices.h)
description: Verifies that the specified headers were understood by the receiver. Note  This function should be called after all headers have been read for a received message.  .
helpviewer_keywords: ["WsCheckMustUnderstandHeaders","WsCheckMustUnderstandHeaders function [Web Services for Windows]","webservices/WsCheckMustUnderstandHeaders","wsw.wscheckmustunderstandheaders"]
old-location: wsw\wscheckmustunderstandheaders.htm
tech.root: wsw
ms.assetid: 28ca98e5-911b-436d-a592-781b832ca6cc
ms.date: 12/05/2018
ms.keywords: WsCheckMustUnderstandHeaders, WsCheckMustUnderstandHeaders function [Web Services for Windows], webservices/WsCheckMustUnderstandHeaders, wsw.wscheckmustunderstandheaders
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
 - WsCheckMustUnderstandHeaders
 - webservices/WsCheckMustUnderstandHeaders
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
 - WsCheckMustUnderstandHeaders
---

# WsCheckMustUnderstandHeaders function


## -description

Verifies that the specified headers were understood by the receiver. 
            <div class="alert"><b>Note</b>  This function should be called after all headers have been read for a received
                message.  </div>
<div> </div>

## -parameters

### -param message [in]

Pointer to the <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> structure containing the headers to be understood.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  where additional error information is stored if the function fails.

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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The message is not in the correct state.
             For more information, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The  validation failed, or the message was not correctly formed.
            

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
Insufficient memory to complete the operation.

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

Because the set of headers is extensible, it is necessary to determine whether a message has  been sufficiently understood to be processed. Therefore, the sender can use this function to indicate which headers must be understood, which headers can be treated as optional or informational.

Standard addressing headers, such as the ones defined in <a href="/windows/desktop/api/webservices/ne-webservices-ws_header_type">WS_HEADER_TYPE</a>, are automatically assumed to be understood, even if they are never read by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsgetheader">WsGetHeader</a>.

Custom, application-defined headers that are read by <a href="/windows/desktop/api/webservices/nf-webservices-wsgetcustomheader">WsGetCustomHeader</a> are also assumed to be understood. Calling <b>WsGetCustomHeader</b> will automatically mark the particular header as understood.

For any  other header processed by the application, the application must explicitly mark the header as understood by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsmarkheaderasunderstood">WsMarkHeaderAsUnderstood</a>. Otherwise, the header is considered to not be understood.

This function should be called after all headers have been read for a received message. An exception to having to call this function is the case of an intermediary that forwards the message to another node without changing its identity (message ID), since the final node will do the check. 



The function will fail if any of the specified headers were not understood. If an error object is supplied to the function, it will be populated with information that can be used to send a fault (see <a href="/windows/desktop/api/webservices/nf-webservices-wscreatefaultfromerror">WsCreateFaultFromError</a>). 



The message must be in the WS_MESSAGE_STATE_READING state.