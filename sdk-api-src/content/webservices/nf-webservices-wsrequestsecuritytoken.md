---
UID: NF:webservices.WsRequestSecurityToken
title: WsRequestSecurityToken function (webservices.h)
description: Get a security token from a security token service (STS) that acts as the token issuer in a federation scenario.
helpviewer_keywords: ["WsRequestSecurityToken","WsRequestSecurityToken function [Web Services for Windows]","webservices/WsRequestSecurityToken","wsw.wsrequestsecuritytoken"]
old-location: wsw\wsrequestsecuritytoken.htm
tech.root: wsw
ms.assetid: ee754a7d-73a9-49ae-afc7-b443fbbe0cce
ms.date: 12/05/2018
ms.keywords: WsRequestSecurityToken, WsRequestSecurityToken function [Web Services for Windows], webservices/WsRequestSecurityToken, wsw.wsrequestsecuritytoken
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
 - WsRequestSecurityToken
 - webservices/WsRequestSecurityToken
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
 - WsRequestSecurityToken
---

# WsRequestSecurityToken function


## -description

Get a security token from a security token service (STS) that acts as
the token issuer in a federation scenario.
This function is used on the client side, and performs the WS-Trust
based negotiation steps with the STS until the security token is
obtained or the negotiation process fails.

## -parameters

### -param channel [in]

The channel on which the negotiation to obtain the security token
should take place.
                

The supplied channel should have been <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannel">created</a> with the appropriate <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_description">WS_SECURITY_DESCRIPTION</a> to meet the security requirements of
the issuer, and then <a href="/windows/desktop/api/webservices/nf-webservices-wsopenchannel">opened</a> to the <a href="/windows/desktop/api/webservices/ns-webservices-ws_endpoint_address">WS_ENDPOINT_ADDRESS</a> of the issuer.  The caller is also
responsible for <a href="/windows/desktop/api/webservices/nf-webservices-wsclosechannel">closing</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wsfreechannel">freeing</a> the channel after the completion of
this function.
                

Thus, the channel must be in state <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_state">WS_CHANNEL_STATE_OPEN</a> when this function is called.  After a successful completion of this
function, the channel will be in state <b>WS_CHANNEL_STATE_OPEN</b>.  After a failed completion, it will
either be in state <b>WS_CHANNEL_STATE_OPEN</b> or state <b>WS_CHANNEL_STATE_FAULTED</b>.

### -param properties

An optional group of settings to be used in the negotiation process
with the issuer.

### -param propertyCount [in]

The number of items in the properties array.

### -param token

The XML security token obtained.  This is set upon successful
completion of the function call, and is unmodified if any failure
occurs during the execution of the function.
                

The returned security token may be used with <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_token_message_security_binding">WS_XML_TOKEN_MESSAGE_SECURITY_BINDING</a> if it is to be
presented to a service.  The token must be freed using <a href="/windows/desktop/api/webservices/nf-webservices-wsfreesecuritytoken">WsFreeSecurityToken</a> when it is no longer needed.

### -param asyncContext [in, optional]

Information on how to invoke the function asynchronously, or <b>NULL</b> if invoking synchronously.

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
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation is still pending.
                

</td>
</tr>
</table>

## -remarks

Windows 7 and Windows Server 2008 R2: WWSAPI only supports <a href="http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf">Ws-Trust</a> and <a href="http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf">Ws-SecureConversation</a> as defined by <a href="/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e">Lightweight Web Services Security Profile (LWSSP)</a>. For details regarding Microsoft's implementation please see the <a href="/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed">MESSAGE Syntax</a> section of LWSSP.