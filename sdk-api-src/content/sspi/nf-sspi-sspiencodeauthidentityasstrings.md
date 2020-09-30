---
UID: NF:sspi.SspiEncodeAuthIdentityAsStrings
title: SspiEncodeAuthIdentityAsStrings function (sspi.h)
description: Encodes the specified authentication identity as three strings.
helpviewer_keywords: ["SspiEncodeAuthIdentityAsStrings","SspiEncodeAuthIdentityAsStrings function [Security]","SspiEncodeAuthIdentityAsStringsA","SspiEncodeAuthIdentityAsStringsW","security.sspiencodeauthidentityasstrings","sspi/SspiEncodeAuthIdentityAsStrings","sspi/SspiEncodeAuthIdentityAsStringsA","sspi/SspiEncodeAuthIdentityAsStringsW"]
old-location: security\sspiencodeauthidentityasstrings.htm
tech.root: security
ms.assetid: 0610a7b8-67e9-4c01-893f-da579eeea2f8
ms.date: 12/05/2018
ms.keywords: SspiEncodeAuthIdentityAsStrings, SspiEncodeAuthIdentityAsStrings function [Security], SspiEncodeAuthIdentityAsStringsA, SspiEncodeAuthIdentityAsStringsW, security.sspiencodeauthidentityasstrings, sspi/SspiEncodeAuthIdentityAsStrings, sspi/SspiEncodeAuthIdentityAsStringsA, sspi/SspiEncodeAuthIdentityAsStringsW
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SspiEncodeAuthIdentityAsStringsW (Unicode) and SspiEncodeAuthIdentityAsStringsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SspiEncodeAuthIdentityAsStrings
 - sspi/SspiEncodeAuthIdentityAsStrings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - SspiCli.dll
api_name:
 - SspiEncodeAuthIdentityAsStrings
 - SspiEncodeAuthIdentityAsStringsA
 - SspiEncodeAuthIdentityAsStringsW
---

# SspiEncodeAuthIdentityAsStrings function


## -description

Encodes the specified authentication identity as three strings.

## -parameters

### -param pAuthIdentity [in]

The credential structure to be encoded.

### -param ppszUserName [out]

The marshaled user name of the identity specified by the <i>pAuthIdentity</i> parameter.

When you have finished using this string, free it by calling the <a href="/windows/desktop/api/sspi/nf-sspi-sspifreeauthidentity">SspiFreeAuthIdentity</a> function.

### -param ppszDomainName [out]

The marshaled domain name of the identity specified by the <i>pAuthIdentity</i> parameter.

When you have finished using this string, free it by calling the <a href="/windows/desktop/api/sspi/nf-sspi-sspifreeauthidentity">SspiFreeAuthIdentity</a> function.

### -param ppszPackedCredentialsString [out]

An encoded string version of a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure that specifies the users credentials.

When you have finished using this string, free it by calling the <a href="/windows/desktop/api/sspi/nf-sspi-sspifreeauthidentity">SspiFreeAuthIdentity</a> function.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
<dt>0xC000000D</dt>
</dl>
</td>
<td width="60%">
The <b>SEC_WINNT_AUTH_IDENTITY_FLAGS_PROCESS_ENCRYPTED</b> flag is set in the identity  structure specified by the <i>pAuthIdentity</i> parameter.

</td>
</tr>
</table>