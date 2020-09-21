---
UID: NF:webservices.WsOpenListener
title: WsOpenListener function (webservices.h)
description: Initiates &quot;listening&quot; on a specified address. Once a listener is opened channels can be accepted from it. If the open is successful the Listener must be closed using the WsCloseListener function before Listener resources can be released.
helpviewer_keywords: ["WsOpenListener","WsOpenListener function [Web Services for Windows]","webservices/WsOpenListener","wsw.wsopenlistener"]
old-location: wsw\wsopenlistener.htm
tech.root: wsw
ms.assetid: 36226881-3fe7-4510-b147-7ee30146482c
ms.date: 12/05/2018
ms.keywords: WsOpenListener, WsOpenListener function [Web Services for Windows], webservices/WsOpenListener, wsw.wsopenlistener
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - WsOpenListener
 - webservices/WsOpenListener
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
 - WsOpenListener
---

# WsOpenListener function


## -description

Initiates "listening" on a specified address.
              Once a listener is opened channels can be accepted
                from it. 
                If the open is successful the Listener must be closed using 
                the <a href="/windows/desktop/api/webservices/nf-webservices-wscloselistener">WsCloseListener</a> function before Listener resources can be released.

## -parameters

### -param listener [in]

A pointer to the <b>Listener</b> object to open.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-listener">WS_LISTENER</a> object and the referenced value may not be <b>NULL</b>.

### -param url [in]

A pointer to a object containing the URL address string for the Listener.  
                

<div class="alert"><b>Note</b>  The URL is always in escaped form..
                The URL may not contain a query string or fragment.
                This URL can include the '+' or '*' wildcards
                    in the host name portion, or a host name, or a literal IP address.
                See Remarks for more information on the URL.</div>
<div> </div>

### -param asyncContext [in, optional]

A pointer  to A WS_ASYNC_CONTEXT object that has information about how to invoke the function asynchronously.  The value is set to <b>NULL</b> if invoking synchronously.

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
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation is still pending.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The listener was aborted during the open, or before the open.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The listener is in the incorrect state.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ADDRESS_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The address is already being used.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ADDRESS_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The address is not valid for this context.

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
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_TIMED_OUT</b></dt>
</dl>
</td>
<td width="60%">
The operation did not complete within the time allotted.

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
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>

## -remarks

When using IPv6 addresses, they must be enclosed in brackets in
                    the host name portion.
                

For more information, see <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a>.
                

For <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_UDP_CHANNEL_BINDING</a>, the path portion of the URL is
                    ignored.  If a literal IP address is specified, then it is used to listen, otherwise
                    a wildcard IP address is used.
                

For <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_TCP_CHANNEL_BINDING</a>, the path portion of the URL is
                    is matched as a prefix against the received URL.  
                    If a literal IP address is specified, then it is used to listen, 
                    otherwise a wildcard IP address is used.