---
UID: NF:winldap.ldap_sasl_bind_sA
title: ldap_sasl_bind_sA function (winldap.h)
description: The ldap_sasl_bind_s function is a synchronous function that authenticates a client to the LDAP server using SASL. (ANSI)
helpviewer_keywords: ["ldap.ldap__sasl__bind__s", "ldap_sasl_bind_sA", "winldap/ldap_sasl_bind_sA"]
old-location: ldap\ldap_sasl_bind_s.htm
tech.root: ldap
ms.assetid: 8347e2f5-bc14-480f-ba96-044ef3280418
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_sasl_bind_s, ldap.ldap__sasl__bind__s, ldap.ldap_sasl_bind_s, ldap_sasl_bind_s, ldap_sasl_bind_s function [LDAP], ldap_sasl_bind_sA, ldap_sasl_bind_sW, winldap/ldap_sasl_bind_s, winldap/ldap_sasl_bind_sA, winldap/ldap_sasl_bind_sW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_sasl_bind_sW (Unicode) and ldap_sasl_bind_sA (ANSI)
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
 - ldap_sasl_bind_sA
 - winldap/ldap_sasl_bind_sA
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
 - ldap_sasl_bind_s
 - ldap_sasl_bind_sA
 - ldap_sasl_bind_sW
---

# ldap_sasl_bind_sA function


## -description

The <b>ldap_sasl_bind_s</b> function is a synchronous function that authenticates a client to the LDAP server using SASL.

## -parameters

### -param ExternalHandle [in]

The session handle.

### -param DistName [in]

The distinguished name of the entry used to bind.

### -param AuthMechanism [in]

Indicates the authentication method to use.

### -param cred [in]

The credentials to use for authentication. Arbitrary credentials can be passed using this parameter. The format and content of the credentials depend on the value of the <i>AuthMechanism</i> argument passed. For more information, see Remarks.

### -param ServerCtrls [in]

A list of LDAP server controls.

### -param ClientCtrls [in]

A list of LDAP client controls.

### -param ServerData [out]

Authentication data returned by the server in response to the bind request.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

The <b>ldap_sasl_bind_s</b> function binds to an LDAP server using the Simple Authentication and Security Layer (SASL) protocol. The bind operation identifies a client to the directory server by providing a distinguished name and some type of authentication credentials. The authentication method being used determines the particular type of credential, and is specified by the <i>AuthMechanism</i> argument. This is passed as a string in the form of "<b>GSSAPI</b>", "<b>GSS-SPNEGO</b>", "<b>DIGEST-MD5</b>", and so on. This function can be used to pass arbitrary credentials to the server, so the application must be ready to interpret the response sent back from the server.

<div class="alert"><b>Note</b>  The Microsoft LDAP client uses a default timeout value of 120 seconds (2 minutes) for each bind-response roundtrip. This timeout value can be changed using the <b>LDAP_OPT_TIMELIMIT</b> session option. Other operations do not have a timeout unless specified using 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a>.</div>
<div> </div>




> [!NOTE]
> The winldap.h header defines ldap_sasl_bind_s as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind_s">ldap_bind_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_sasl_binda">ldap_sasl_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind_s">ldap_simple_bind_s</a>
