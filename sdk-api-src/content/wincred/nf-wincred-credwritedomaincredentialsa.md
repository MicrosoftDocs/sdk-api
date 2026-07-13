---
UID: NF:wincred.CredWriteDomainCredentialsA
title: CredWriteDomainCredentialsA function (wincred.h)
description: Writes domain credentials to the user's credential set. (ANSI)
helpviewer_keywords: ["CRED_PRESERVE_CREDENTIAL_BLOB", "CredWriteDomainCredentialsA", "wincred/CredWriteDomainCredentialsA"]
old-location: security\credwritedomaincredentials.htm
tech.root: security
ms.assetid: 6b54c14f-a736-4fb0-b4e4-97765a792a5e
ms.date: 12/05/2018
ms.keywords: CRED_PRESERVE_CREDENTIAL_BLOB, CredWriteDomainCredentials, CredWriteDomainCredentials function [Security], CredWriteDomainCredentialsA, CredWriteDomainCredentialsW, _cred_credwritedomaincredentials, security.credwritedomaincredentials, wincred/CredWriteDomainCredentials, wincred/CredWriteDomainCredentialsA, wincred/CredWriteDomainCredentialsW
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredWriteDomainCredentialsW (Unicode) and CredWriteDomainCredentialsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredWriteDomainCredentialsA
 - wincred/CredWriteDomainCredentialsA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-0.dll
 - sechost.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
 - CredWriteDomainCredentials
 - CredWriteDomainCredentialsA
 - CredWriteDomainCredentialsW
---

# CredWriteDomainCredentialsA function


## -description

The <b>CredWriteDomainCredentials</b> function writes domain credentials to the user's credential set. The credential set used is the one associated with the logon session of the current token. The token must not have the user's SID disabled.

## -parameters

### -param TargetInfo [in]

Identifies the target server. At least one of the naming members must be non-<b>NULL</b> and can be <b>NetbiosServerName</b>, <b>DnsServerName</b>, <b>NetbiosDomainName</b>, <b>DnsDomainName</b>, or <b>DnsTreeName</b>.

### -param Credential [in]

Credential to be written. 




The credential must be one that matches <i>TargetInfo</i> For instance, if the <b>TargetName</b> is a wildcard DNS name, then the <b>TargetName</b> member of the credential must be a postfix of the <b>DnsServerName</b> member from the <i>TargetInfo</i>.

### -param Flags [in]

Flags to control the operation of the API. The following flag is defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRED_PRESERVE_CREDENTIAL_BLOB"></a><a id="cred_preserve_credential_blob"></a><dl>
<dt><b>CRED_PRESERVE_CREDENTIAL_BLOB</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The credential BLOB should be preserved from the already existing credential with the same credential name and credential type. The <b>CredentialBlobSize</b> of the passed in <i>Credential</i> structure must be zero.

</td>
</tr>
</table>

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. Call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get a more specific status code. The following status codes can be returned.

Other smart card errors can be returned when writing a CRED_TYPE_CERTIFICATE credential.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters are not valid. Either none of the naming parameters were specified, or the credential specified did not have the <b>Type</b> member set to CRED_TYPE_DOMAIN_PASSWORD or CRED_TYPE_DOMAIN_CERTIFICATE, or the <i>Credential</i> does not match the <i>TargetInfo</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_LOGON_SESSION</b></dt>
</dl>
</td>
<td width="60%">
The logon session does not exist or there is no credential set associated with this logon session. Network logon sessions do not have an associated credential set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
A value that is not valid was specified for the <i>Flags</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_USERNAME</b></dt>
</dl>
</td>
<td width="60%">
The <b>UserName</b> member of the passed in <i>Credential</i> structure is not valid. For a description of valid syntaxes, see the definition of that member.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
CRED_PRESERVE_CREDENTIAL_BLOB was specified and there is no existing credential by the same <b>TargetName</b> and <b>Type</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_E_NO_READERS_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The CRED_TYPE_CERTIFICATE credential being written requires the smart card reader to be available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_E_NO_SMARTCARD or SCARD_W_REMOVED_CARD: The CRED_TYPE_CERTIFICATE</b></dt>
</dl>
</td>
<td width="60%">
The credential being written requires the smart card to be inserted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_W_WRONG_CHV</b></dt>
</dl>
</td>
<td width="60%">
The wrong PIN was supplied for the CRED_TYPE_CERTIFICATE credential being written.

</td>
</tr>
</table>

## -remarks

When this function writes a CRED_TYPE_CERTIFICATE credential, the <i>Credential</i>-&gt;<b>CredentialBlob</b> member specifies the PIN that protects the private key of the certificate specified by the <i>Credential</i>-&gt;<b>UserName</b>. The credential manager does not maintain the PIN. Rather, the PIN is passed to the CSP of the certificate for later use by the CSP and authentication packages. The CSP defines the lifetime of the PIN. For instance, most CSPs flush the PIN upon smart card removal.

<b>CredWriteDomainCredentials</b> differs from <a href="/windows/desktop/api/wincred/nf-wincred-credwritea">CredWrite</a> in that it handles the idiosyncrasies of domain (CRED_TYPE_DOMAIN_PASSWORD or CRED_TYPE_DOMAIN_CERTIFICATE) credentials. Domain credentials contain more than one target member.

If the value of the <b>Type</b> member of the <a href="/windows/desktop/api/wincred/ns-wincred-credentiala">CREDENTIAL</a> structure specified by the <i>Credential</i>  parameter is <b>CRED_TYPE_DOMAIN_EXTENDED</b>, a namespace must be specified in the target name.




> [!NOTE]
> The wincred.h header defines CredWriteDomainCredentials as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
