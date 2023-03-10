---
UID: NF:sspi.SspiEncodeStringsAsAuthIdentity
title: SspiEncodeStringsAsAuthIdentity function (sspi.h)
description: Encodes a set of three credential strings as an authentication identity structure.
helpviewer_keywords: ["SspiEncodeStringsAsAuthIdentity","SspiEncodeStringsAsAuthIdentity function [Security]","security.sspiencodestringsasauthidentity","sspi/SspiEncodeStringsAsAuthIdentity"]
old-location: security\sspiencodestringsasauthidentity.htm
tech.root: security
ms.assetid: 0aea2f00-fcf1-4c4e-a22f-a669dd4fb294
ms.date: 12/05/2018
ms.keywords: SspiEncodeStringsAsAuthIdentity, SspiEncodeStringsAsAuthIdentity function [Security], security.sspiencodestringsasauthidentity, sspi/SspiEncodeStringsAsAuthIdentity
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - SspiEncodeStringsAsAuthIdentity
 - sspi/SspiEncodeStringsAsAuthIdentity
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
 - SspiEncodeStringsAsAuthIdentity
---

# SspiEncodeStringsAsAuthIdentity function


## -description

Encodes a set of three credential strings as an authentication identity structure.

## -parameters

### -param pszUserName [in]

The user name associated with the identity to encode.

### -param pszDomainName [in]

The domain name associated with the identity to encode.

### -param pszPackedCredentialsString [in]

An encoded string version of a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX2</a> structure that specifies the user's credentials.

### -param ppAuthIdentity [out]

A pointer to the encoded identity structure.

When you have finished using this structure, free it by calling the <a href="/windows/desktop/api/sspi/nf-sspi-sspifreeauthidentity">SspiFreeAuthIdentity</a> function.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.