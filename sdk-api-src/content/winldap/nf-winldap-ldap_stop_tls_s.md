---
UID: NF:winldap.ldap_stop_tls_s
title: ldap_stop_tls_s function (winldap.h)
description: Stops the encryption operation started by a call to ldap_start_tls_s.
helpviewer_keywords: ["ldap.ldap_stop_tls_s","ldap_stop_tls_s","ldap_stop_tls_s function [LDAP]","winldap/ldap_stop_tls_s"]
old-location: ldap\ldap_stop_tls_s.htm
tech.root: ldap
ms.assetid: 7b82e79f-009e-4224-b4ce-12b60e0c1011
ms.date: 12/05/2018
ms.keywords: ldap.ldap_stop_tls_s, ldap_stop_tls_s, ldap_stop_tls_s function [LDAP], winldap/ldap_stop_tls_s
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
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldap_stop_tls_s
 - winldap/ldap_stop_tls_s
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_stop_tls_s
---

# ldap_stop_tls_s function


## -description

The <b>ldap_stop_tls_s</b> function stops the encryption operation started by a call to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_start_tls_sa">ldap_start_tls_s</a>.

## -parameters

### -param ExternalHandle [in]

A pointer to an <b>LDAP</b> structure that represents the current session.

## -returns

Returns <b>TRUE</b> if the function call succeeds. Returns <b>FALSE</b> if a bind is currently in progress on the connection, if the connection is not actively connected to the server, or if TLS (SSL) negotiation is in progress on the connection.

## -remarks

The <b>ldap_stop_tls_s</b> function should only be called on a connection for which TLS (SSL) was established by using <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_start_tls_sa">ldap_start_tls_s</a>. It should not be called on a TLS (SSL) connection established by some other function, such as <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_sslinit">ldap_sslinit</a>. Any outstanding requests on the connection will be abandoned before TLS encryption is terminated. If this function fails, that is, returns <b>FALSE</b>, close the connection by using <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> or <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind_s">ldap_unbind_s</a> because the connection can be left in an indeterminate state.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/using-start-stop-tls-encryption">Using Start-stop TLS Encryption</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_start_tls_sa">ldap_start_tls_s</a>