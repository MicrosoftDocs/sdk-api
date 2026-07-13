---
UID: NF:wincred.CredWriteW
title: CredWriteW function (wincred.h)
description: Creates a new credential or modifies an existing credential in the user's credential set. (Unicode)
helpviewer_keywords: ["CRED_PRESERVE_CREDENTIAL_BLOB", "CredWrite", "CredWrite function [Security]", "CredWriteW", "_cred_credwrite", "security.credwrite", "wincred/CredWrite", "wincred/CredWriteW"]
old-location: security\credwrite.htm
tech.root: security
ms.assetid: 9a590347-d610-4916-bf63-60fbec173ac2
ms.date: 12/05/2018
ms.keywords: CRED_PRESERVE_CREDENTIAL_BLOB, CredWrite, CredWrite function [Security], CredWriteA, CredWriteW, _cred_credwrite, security.credwrite, wincred/CredWrite, wincred/CredWriteA, wincred/CredWriteW
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredWriteW (Unicode) and CredWriteA (ANSI)
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
 - CredWriteW
 - wincred/CredWriteW
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
 - CredWrite
 - CredWriteA
 - CredWriteW
---

# CredWriteW function


## -description

The <b>CredWrite</b> function creates a new credential or modifies an existing credential in the user's credential set. The new credential is associated with the logon session of the current token. The token must not have the user's <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) disabled.

## -parameters

### -param Credential [in]

A pointer to the <a href="/windows/desktop/api/wincred/ns-wincred-credentiala">CREDENTIAL</a> structure to be written.

### -param Flags [in]

Flags that control the function's operation. The following flag is defined.

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
The credential BLOB from an existing credential is preserved with the same credential name and credential type. The <b>CredentialBlobSize</b> of the passed in <i>Credential</i> structure must be zero.

</td>
</tr>
</table>

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. Call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get a more specific status code. The following status codes can be returned.

Other smart card errors can be returned when writing a CRED_TYPE_CERTIFICATE credential.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_LOGON_SESSION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The logon session does not exist or there is no credential set associated with this logon session. Network logon sessions do not have an associated credential set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Certain fields cannot be changed in an existing credential. This error is returned if a field does not match the value in a protected field of the existing credential.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
<dt></dt>
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
<dt></dt>
</dl>
</td>
<td width="60%">
The <b>UserName</b> member of the passed in <i>Credential</i> structure is not valid. For a description of valid user name syntax, see the definition of that member.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
<dt></dt>
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
<dt></dt>
</dl>
</td>
<td width="60%">
The CRED_TYPE_CERTIFICATE credential being written requires the smart card reader to be available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_E_NO_SMARTCARD or SCARD_W_REMOVED_CARD</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
A CRED_TYPE_CERTIFICATE credential being written requires the smart card to be inserted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_W_WRONG_CHV</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The wrong PIN was supplied for the CRED_TYPE_CERTIFICATE credential being written.

</td>
</tr>
</table>

## -remarks

This function creates a credential if a credential with the specified <b>TargetName</b> and <b>Type</b> does not exist. If a credential with the specified <b>TargetName</b> and <b>Type</b> exists, the new specified credential replaces the existing one.

When this function writes a CRED_TYPE_CERTIFICATE credential, the <i>Credential</i>-&gt;<b>CredentialBlob</b> member specifies the PIN protecting the private key of the certificate specified by the <i>Credential</i>-&gt;<b>UserName</b> member. The credential manager does not maintain the PIN. Rather, the PIN is passed to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) indicated on the certificate for later use by the CSP and the authentication packages. The CSP defines the lifetime of the PIN. Most CSPs flush the PIN when the smart card removal from the smart card reader.

If the value of the <b>Type</b> member of the <a href="/windows/desktop/api/wincred/ns-wincred-credentiala">CREDENTIAL</a> structure specified by the <i>Credential</i>  parameter is <b>CRED_TYPE_DOMAIN_EXTENDED</b>, a namespace must be specified in the target name. This function does not support writing to target names that contain wildcards. 





> [!NOTE]
> The wincred.h header defines CredWrite as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincred/ns-wincred-credentiala">CREDENTIAL</a>
