---
UID: NS:wincrypt._HTTPSPolicyCallbackData
title: HTTPSPolicyCallbackData (wincrypt.h)
description: Holds policy information used in the verification of Secure Sockets Layer (SSL) client/server certificate chains.
helpviewer_keywords: ["*PHTTPSPolicyCallbackData","*PSSL_EXTRA_CERT_CHAIN_POLICY_PARA","AUTHTYPE_CLIENT","AUTHTYPE_SERVER","HTTPSPolicyCallbackData","HTTPSPolicyCallbackData structure [Security]","PHTTPSPolicyCallbackData","PHTTPSPolicyCallbackData structure pointer [Security]","PSSL_EXTRA_CERT_CHAIN_POLICY_PARA","PSSL_EXTRA_CERT_CHAIN_POLICY_PARA structure pointer [Security]","SECURITY_FLAG_IGNORE_CERT_CN_INVALID","SECURITY_FLAG_IGNORE_CERT_DATE_INVALID","SECURITY_FLAG_IGNORE_REVOCATION","SECURITY_FLAG_IGNORE_UNKNOWN_CA","SECURITY_FLAG_IGNORE_WRONG_USAGE","SSL_EXTRA_CERT_CHAIN_POLICY_PARA","SSL_EXTRA_CERT_CHAIN_POLICY_PARA structure [Security]","security.ssl_extra_cert_chain_policy_para","wincrypt/PHTTPSPolicyCallbackData","wincrypt/PSSL_EXTRA_CERT_CHAIN_POLICY_PARA","wincrypt/SSL_EXTRA_CERT_CHAIN_POLICY_PARA"]
old-location: security\ssl_extra_cert_chain_policy_para.htm
tech.root: security
ms.assetid: 3422693a-3fad-4ed8-9fab-d9a185476123
ms.date: 12/05/2018
ms.keywords: '*PHTTPSPolicyCallbackData, *PSSL_EXTRA_CERT_CHAIN_POLICY_PARA, AUTHTYPE_CLIENT, AUTHTYPE_SERVER, HTTPSPolicyCallbackData, HTTPSPolicyCallbackData structure [Security], PHTTPSPolicyCallbackData, PHTTPSPolicyCallbackData structure pointer [Security], PSSL_EXTRA_CERT_CHAIN_POLICY_PARA, PSSL_EXTRA_CERT_CHAIN_POLICY_PARA structure pointer [Security], SECURITY_FLAG_IGNORE_CERT_CN_INVALID, SECURITY_FLAG_IGNORE_CERT_DATE_INVALID, SECURITY_FLAG_IGNORE_REVOCATION, SECURITY_FLAG_IGNORE_UNKNOWN_CA, SECURITY_FLAG_IGNORE_WRONG_USAGE, SSL_EXTRA_CERT_CHAIN_POLICY_PARA, SSL_EXTRA_CERT_CHAIN_POLICY_PARA structure [Security], security.ssl_extra_cert_chain_policy_para, wincrypt/PHTTPSPolicyCallbackData, wincrypt/PSSL_EXTRA_CERT_CHAIN_POLICY_PARA, wincrypt/SSL_EXTRA_CERT_CHAIN_POLICY_PARA'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: HTTPSPolicyCallbackData, *PHTTPSPolicyCallbackData, SSL_EXTRA_CERT_CHAIN_POLICY_PARA, *PSSL_EXTRA_CERT_CHAIN_POLICY_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTPSPolicyCallbackData
 - wincrypt/_HTTPSPolicyCallbackData
 - PHTTPSPolicyCallbackData
 - wincrypt/PHTTPSPolicyCallbackData
 - HTTPSPolicyCallbackData
 - wincrypt/HTTPSPolicyCallbackData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - HTTPSPolicyCallbackData
---

# HTTPSPolicyCallbackData structure


## -description

The <b>SSL_EXTRA_CERT_CHAIN_POLICY_PARA</b> structure, also identified by the name <b>HTTPSPolicyCallbackData</b>,  holds policy information used in the verification of <a href="/windows/desktop/SecGloss/s-gly">Secure Sockets Layer</a> (SSL) client/server certificate chains.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.cbStruct

<b>DWORD</b> value that specifies the number of bytes in this structure.

### -field DUMMYUNIONNAME.cbSize

<b>DWORD</b> value that specifies the size, in bytes,  of this structure.

### -field dwAuthType

<b>DWORD</b> value that specifies the type of authentication. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AUTHTYPE_CLIENT"></a><a id="authtype_client"></a><dl>
<dt><b>AUTHTYPE_CLIENT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The client is being authenticated.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHTYPE_SERVER"></a><a id="authtype_server"></a><dl>
<dt><b>AUTHTYPE_SERVER</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The server is being authenticated.

</td>
</tr>
</table>

### -field fdwChecks

<b>DWORD</b> value that specifies certificate errors to ignore. This can be a bitwise combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECURITY_FLAG_IGNORE_REVOCATION"></a><a id="security_flag_ignore_revocation"></a><dl>
<dt><b>SECURITY_FLAG_IGNORE_REVOCATION</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Ignore errors associated with a revoked certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></a><a id="security_flag_ignore_unknown_ca"></a><dl>
<dt><b>SECURITY_FLAG_IGNORE_UNKNOWN_CA</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Ignore errors associated with an unknown <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></a><a id="security_flag_ignore_wrong_usage"></a><dl>
<dt><b>SECURITY_FLAG_IGNORE_WRONG_USAGE</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Ignore errors associated with the use of a certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></a><a id="security_flag_ignore_cert_cn_invalid"></a><dl>
<dt><b>SECURITY_FLAG_IGNORE_CERT_CN_INVALID</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
Ignore errors associated with a certificate that contains a common name that is not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></a><a id="security_flag_ignore_cert_date_invalid"></a><dl>
<dt><b>SECURITY_FLAG_IGNORE_CERT_DATE_INVALID</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Ignore errors associated with an expired certificate.

</td>
</tr>
</table>

### -field pwszServerName

A pointer to a null-terminated wide character string that contains the server name. This member is ignored if the value of the <b>dwAuthType</b> member is <b>AUTHTYPE_CLIENT</b>.

If the string is Punycode encoded, then the server name from the certificate, either the DNS name or common name, is converted to a Punycode encoded string. Matching is then performed, label-by-label if the name contains wildcards, or a case-insensitive exact match otherwise. 

If the string contains Unicode characters outside of the ASCII character set and the subject name, either the DNS name or common name, is a Punycode encoded string then it is Punycode encoded before comparison.