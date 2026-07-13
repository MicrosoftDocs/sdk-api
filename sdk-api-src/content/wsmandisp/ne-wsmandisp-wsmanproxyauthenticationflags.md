---
UID: NE:wsmandisp._WSManProxyAuthenticationFlags
title: WSManProxyAuthenticationFlags (wsmandisp.h)
description: Determines the proxy authentication mechanism.
helpviewer_keywords: ["WSManFlagProxyAuthenticationUseBasic","WSManFlagProxyAuthenticationUseDigest","WSManFlagProxyAuthenticationUseNegotiate","WSManProxyAuthenticationFlags","WSManProxyAuthenticationFlags enumeration [Windows Remote Management]","winrm.wsmanproxyauthenticationflags","wsmandisp/WSManFlagProxyAuthenticationUseBasic","wsmandisp/WSManFlagProxyAuthenticationUseDigest","wsmandisp/WSManFlagProxyAuthenticationUseNegotiate","wsmandisp/WSManProxyAuthenticationFlags"]
old-location: winrm\wsmanproxyauthenticationflags.htm
tech.root: winrm
ms.assetid: 4a86dfae-18c9-4865-8b8b-bb0ac01f558c
ms.date: 12/05/2018
ms.keywords: WSManFlagProxyAuthenticationUseBasic, WSManFlagProxyAuthenticationUseDigest, WSManFlagProxyAuthenticationUseNegotiate, WSManProxyAuthenticationFlags, WSManProxyAuthenticationFlags enumeration [Windows Remote Management], winrm.wsmanproxyauthenticationflags, wsmandisp/WSManFlagProxyAuthenticationUseBasic, wsmandisp/WSManFlagProxyAuthenticationUseDigest, wsmandisp/WSManFlagProxyAuthenticationUseNegotiate, wsmandisp/WSManProxyAuthenticationFlags
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSManProxyAuthenticationFlags
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSManProxyAuthenticationFlags
 - wsmandisp/_WSManProxyAuthenticationFlags
 - WSManProxyAuthenticationFlags
 - wsmandisp/WSManProxyAuthenticationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WSManDisp.h
api_name:
 - WSManProxyAuthenticationFlags
---

# WSManProxyAuthenticationFlags enumeration


## -description

Determines the proxy authentication mechanism.

## -enum-fields

### -field WSManFlagProxyAuthenticationUseNegotiate:0x1

Use Negotiate authentication. The client sends a request to the server to authenticate. The server determines whether to use Kerberos or NTLM. In general, Kerberos is selected to authenticate a domain account and NTLM is selected for local computer accounts. But there are also some special cases in which Kerberos/NTLM are selected. The user name should be specified in the form DOMAIN\username for a domain user or SERVERNAME\username for a local user on a server computer.

### -field WSManFlagProxyAuthenticationUseBasic:0x2

Use Basic authentication. The client presents credentials in the form of a user name and password that are directly transmitted in the request message.

### -field WSManFlagProxyAuthenticationUseDigest:0x4

Use Digest authentication. Only the client computer can initiate a Digest authentication request. The client sends a request to the server to authenticate and receives from the server a token string. The client then sends the resource request, including the user name and a cryptographic hash of the password combined with the token string. Digest authentication is supported for HTTP and HTTPS.

