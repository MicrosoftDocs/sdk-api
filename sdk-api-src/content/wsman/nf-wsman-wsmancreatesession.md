---
UID: NF:wsman.WSManCreateSession
title: WSManCreateSession function (wsman.h)
description: Creates a session object.
helpviewer_keywords: ["WSManCreateSession","WSManCreateSession function [Windows Remote Management]","winrm.wsmancreatesession","wsman/WSManCreateSession"]
old-location: winrm\wsmancreatesession.htm
tech.root: winrm
ms.assetid: 5123d876-5123-4fa4-8f6f-859a26aad825
ms.date: 12/05/2018
ms.keywords: WSManCreateSession, WSManCreateSession function [Windows Remote Management], winrm.wsmancreatesession, wsman/WSManCreateSession
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManCreateSession
 - wsman/WSManCreateSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManCreateSession
---

# WSManCreateSession function


## -description

Creates a session object.

## -parameters

### -param apiHandle [in]

Specifies the API handle returned by the <a href="/windows/desktop/api/wsman/nf-wsman-wsmaninitialize">WSManInitialize</a> call. This parameter cannot be <b>NULL</b>.

### -param connection [in, optional]

Indicates to which protocol and agent to connect. If this parameter is <b>NULL</b>, the 
       connection will default to localhost (127.0.0.1). This parameter can be a simple host name or a complete URL. 
       The format is the following:

[transport://]host[:port][/prefix] where:

<table>
<tr>
<th>Element</th>
<th>Description</th>
</tr>
<tr>
<td>
transport

</td>
<td>
Either HTTP or HTTPS. Default is HTTP.

</td>
</tr>
<tr>
<td>
host

</td>
<td>
Can be in a DNS name, NetBIOS name, or IP address.

</td>
</tr>
<tr>
<td>
port

</td>
<td>
Defaults to 80 for HTTP and to 443 for HTTPS. The defaults can be changed in the local configuration.

</td>
</tr>
<tr>
<td>
prefix

</td>
<td>
Any string. Default is "wsman". The default can be changed in the local configuration.

</td>
</tr>
</table>

### -param flags

Reserved for future use. Must be zero.

### -param serverAuthenticationCredentials [in, optional]

Defines the authentication method such as Negotiate, Kerberos, Digest, Basic, or client certificate. If the authentication mechanism is Negotiate, Kerberos, Digest, or Basic, the structure can also contain the credentials used for authentication. If  client certificate authentication is used, the certificate thumbprint must be specified.

If credentials are specified, this parameter contains the user name and password of a local account or domain account. If this parameter is <b>NULL</b>, the default credentials are used. The default credentials are the credentials that the current thread is executing under. The client must explicitly specify the credentials when Basic or Digest authentication is used. If explicit credentials are used, both the user name and the password must be valid. For more information about the authentication credentials, see the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_authentication_credentials">WSMAN_AUTHENTICATION_CREDENTIALS</a> structure.

### -param proxyInfo [in, optional]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_proxy_info">WSMAN_PROXY_INFO</a> structure that specifies proxy information. This value can be <b>NULL</b>.

### -param session [out]

Defines the session handle that uniquely identifies the session. This parameter cannot be <b>NULL</b>. This handle  should be closed by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanclosesession">WSManCloseSession</a> method.

## -returns

If the function succeeds, the return value is zero. Otherwise, the return value is an error code.