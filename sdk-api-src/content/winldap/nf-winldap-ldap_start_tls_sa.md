---
UID: NF:winldap.ldap_start_tls_sA
title: ldap_start_tls_sA function (winldap.h)
description: Used in an active LDAP session to begin using TLS encryption. (ANSI)
helpviewer_keywords: ["ldap_start_tls_sA", "winldap/ldap_start_tls_sA"]
old-location: ldap\ldap_start_tls_s.htm
tech.root: ldap
ms.assetid: faca9324-5a85-47b0-9d6a-c62ec3c1ee80
ms.date: 12/05/2018
ms.keywords: ldap.ldap_start_tls_s, ldap_start_tls_s, ldap_start_tls_s function [LDAP], ldap_start_tls_sA, ldap_start_tls_sW, winldap/ldap_start_tls_s, winldap/ldap_start_tls_sA, winldap/ldap_start_tls_sW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_start_tls_sW (Unicode) and ldap_start_tls_sA (ANSI)
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
 - ldap_start_tls_sA
 - winldap/ldap_start_tls_sA
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
 - ldap_start_tls_s
 - ldap_start_tls_sA
 - ldap_start_tls_sW
---

# ldap_start_tls_sA function


## -description

The <b>ldap_start_tls_s</b> function is used in an active LDAP session to begin using TLS encryption.

## -parameters

### -param ExternalHandle [in]

A pointer to an <b>LDAP</b> structure that represents the current session.

### -param ServerReturnValue [out]

Optional. A pointer to a <b>ULONG</b> that may contain a server error code. This parameter should be consulted if <b>LDAP_OTHER</b> is returned in the return value.  Pass in <b>NULL</b> if you do not wish to use it.

### -param result [out]

Optional. A pointer to a pointer for an <a href="/windows/desktop/api/winldap/ns-winldap-ldapmessage">LDAPMessage</a>  structure that may contain a server referral message.  Pass in <b>NULL</b> if you do not wish to use it.

### -param ServerControls [in]

Optional. A NULL-terminated array of pointers to  <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapcontrola">LDAPControl</a> structures that represent server controls.  Pass in <b>NULL</b> if you do not want to specify server  controls.

### -param ClientControls [in]

Optional. A NULL-terminated array of pointers to <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapcontrola">LDAPControl</a> structures that represent client controls.  Pass in <b>NULL</b> if you do not want to specify client controls.

## -returns

If the function call succeeds, <b>LDAP_SUCCESS</b> is returned. <b>LDAP_UNWILLING_TO_PERFORM</b> is returned if a TLD/SSL session is already in progress, or if a bind is currently in progress, or if there is an outstanding LDAP request on the connection. If the server rejects the extended operation, <b>LDAP_OTHER</b> is returned and the <i>ServerReturnValue</i> parameter should be checked for the server error code.

## -remarks

The <b>ldap_start_tls_s</b> function is called on an existing LDAP session to initiate the use of  TLS (SSL) encryption. The connection must not already have TLS (SSL) encryption enabled, and neither signing nor sealing can already be enabled. Also, a bind cannot be currently in progress on the connection, nor can there be any outstanding LDAP requests on the connection. If these conditions are not met, <b>LDAP_UNWILLING_TO_PERFORM</b> is returned. If these conditions are met, the function will send the appropriate extended operation to the server to initiate TLS (SSL), and then negotiate the encryption with the server. If the server rejects the extended operation, <b>LDAP_OTHER</b> will be returned, and the <i>ServerReturnValue</i> should be checked to retrieve the server error code.

It is possible that the server will return a referral in response to this call. For security reasons, the referral will not be automatically chased. A pointer to the referral message is returned in the <i>result</i> parameter.

After <b>ldap_start_tls_s</b> is called, automatic referral chasing and autoreconnect are disabled on the connection. They will be restored to their previous settings upon successful completion of the <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_stop_tls_s">ldap_stop_tls_s</a> operation.

This function has a default timeout of about thirty seconds. That timeout is used in waiting for responses from the server for the Start TLS extended operation and during the TLS (SSL) negotiation.

For more information about start-stop TLS encryption, see <a href="/previous-versions/windows/desktop/ldap/using-start-stop-tls-encryption">Using Start-Stop TLS Encryption</a>.


> [!NOTE]
> The winldap.h header defines ldap_start_tls_s as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/using-start-stop-tls-encryption">Using Start-Stop TLS Encryption</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_stop_tls_s">ldap_stop_tls_s</a>
