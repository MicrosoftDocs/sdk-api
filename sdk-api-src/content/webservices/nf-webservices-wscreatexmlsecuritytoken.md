---
UID: NF:webservices.WsCreateXmlSecurityToken
title: WsCreateXmlSecurityToken function (webservices.h)
description: Creates a security token from its specified XML form.
helpviewer_keywords: ["WsCreateXmlSecurityToken","WsCreateXmlSecurityToken function [Web Services for Windows]","webservices/WsCreateXmlSecurityToken","wsw.wscreatexmlsecuritytoken"]
old-location: wsw\wscreatexmlsecuritytoken.htm
tech.root: wsw
ms.assetid: 1d82c6c3-2bcf-4883-aed7-1a163bbb2228
ms.date: 12/05/2018
ms.keywords: WsCreateXmlSecurityToken, WsCreateXmlSecurityToken function [Web Services for Windows], webservices/WsCreateXmlSecurityToken, wsw.wscreatexmlsecuritytoken
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
 - WsCreateXmlSecurityToken
 - webservices/WsCreateXmlSecurityToken
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
 - WsCreateXmlSecurityToken
---

# WsCreateXmlSecurityToken function


## -description

Creates a security token from its specified XML form.

## -parameters

### -param tokenXml [in]

Pointer to a <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> structure containing  the security token in its XML form.    The referenced buffer must have exactly
one top level XML element.

### -param tokenKey [in, optional]

Pointer to a <b>SECURITY_KEY_HANDLE</b> structure that may or may not contain a cryptographic proof-of-possession key. If present the key can be used to bind
this security token to a message.  If the value of the <i>tokenKey</i> parameter is not <b>NULL</b>, the token is
assumed to have a proof-of-possession key.  If the value  is <b>NULL</b>, the structure is
assumed to be a "bearer token" as defined below.

<ul>
<li> A bearer token also called a basic or keyless token is serialized in a message to demonstrate
the message's possession of the token, and to indicate the intention to apply the claims from the token to that message.



</li>
<li> A proof-of-possession token also called a PoP or
cryptographic token has an associated
cryptographic key which must be used to "sign" a message in order to
demonstrate possession of the token and to indicate the intention to
apply the claims from the token to that message.  An example is an
X.509 certificate: the message must be signed with the private key of
the certificate in order for a receiving principal to accept the
message as carrying the claims present in the certificate.

</li>
</ul>

### -param properties

An array of  <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_security_token_property">WS_XML_SECURITY_TOKEN_PROPERTY</a> structures containing optional properties for the XML security token.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).

### -param propertyCount [in]

The number of properties in the <i>properties</i> array.

### -param token

On   success, a pointer that receives the address of the  <a href="/windows/desktop/wsw/ws-security-token">WS_SECURITY_TOKEN</a> structure representing the created XML security token.
                
When you no longer need this structure, you must free it by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsfreesecuritytoken">WsFreeSecurityToken</a>.
                

The returned security token may be used with <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_token_message_security_binding">WS_XML_TOKEN_MESSAGE_SECURITY_BINDING</a> if it is to be

presented to a service.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

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