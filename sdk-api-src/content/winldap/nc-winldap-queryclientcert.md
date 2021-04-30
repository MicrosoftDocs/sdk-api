---
UID: NC:winldap.QUERYCLIENTCERT
title: QUERYCLIENTCERT (winldap.h)
description: Enables the server to request a certificate from the client when establishing a Secure Sockets Layer (SSL) connection.
helpviewer_keywords: ["QUERYCLIENTCERT","QUERYCLIENTCERT callback","QUERYCLIENTCERT callback function [LDAP]","_ldap_queryclientcert","ldap.queryclientcert","winldap/QUERYCLIENTCERT"]
old-location: ldap\queryclientcert.htm
tech.root: ldap
ms.assetid: c2788fb9-14db-41d2-9555-ae264f825121
ms.date: 12/05/2018
ms.keywords: QUERYCLIENTCERT, QUERYCLIENTCERT callback, QUERYCLIENTCERT callback function [LDAP], _ldap_queryclientcert, ldap.queryclientcert, winldap/QUERYCLIENTCERT
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QUERYCLIENTCERT
 - winldap/QUERYCLIENTCERT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winldap.h
api_name:
 - QUERYCLIENTCERT
---

## -description

The <b>QUERYCLIENTCERT</b> function is a client-side function that enables the server to request a certificate from the client when establishing a Secure Sockets Layer (SSL) connection.

Also see [Desktop Win32 code samples](/windows/win32/desktop-win32-code-samples).

## -parameters

### -param Connection [in]

The session handle.

### -param trusted_CAs [in]

A list of server-trusted Certificate Authorities.

### -param ppCertificate [in, out]

Upon receiving the callback, the user supplies an appropriate client certificate in 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> format and returns a value of <b>TRUE</b>. If the client cannot supply an appropriate certificate or wants the server to use anonymous credentials, it should return a value of <b>FALSE</b> instead. Any certificate supplied must be freed by the application after the connection is completed.

## -remarks

Implement this function in your client application with the signature previously described. Then call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a> (conn, LDAP_OPT_CLIENT_CERTIFICATE, &amp;CertRoutine) where CertRoutine is the address of your callback routine.

When the server demands a client certificate for authorization it will call <b>QUERYCLIENTCERT</b>. The LDAP run time passes a structure containing a list of server-trusted Certificate Authorities. The client application must examine this list of CAs the server trusts and supply an appropriate client certificate. The run time subsequently passes these credentials back to the SSL server as part of the handshake. If the client application requires anonymous credentials, it should pass back <b>FALSE</b> instead of supplying a certificate.

<div class="alert"><b>Note</b>  The application must perform an external bind subsequent to establishing the connection for the server to use the supplied client credentials.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>

<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a>

[Desktop Win32 code samples](/windows/win32/desktop-win32-code-samples)
