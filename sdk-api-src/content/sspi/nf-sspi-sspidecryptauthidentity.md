---
UID: NF:sspi.SspiDecryptAuthIdentity
title: SspiDecryptAuthIdentity function (sspi.h)
description: Decrypts the specified encrypted credential.
helpviewer_keywords: ["SspiDecryptAuthIdentity","SspiDecryptAuthIdentity function [Security]","security.sspidecryptauthidentity","sspi/SspiDecryptAuthIdentity"]
old-location: security\sspidecryptauthidentity.htm
tech.root: security
ms.assetid: aef0206c-c376-4877-b1a6-5e86d2e35dea
ms.date: 12/05/2018
ms.keywords: SspiDecryptAuthIdentity, SspiDecryptAuthIdentity function [Security], security.sspidecryptauthidentity, sspi/SspiDecryptAuthIdentity
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
 - SspiDecryptAuthIdentity
 - sspi/SspiDecryptAuthIdentity
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
 - SspiDecryptAuthIdentity
---

# SspiDecryptAuthIdentity function


## -description

Decrypts the specified  encrypted credential.

## -parameters

### -param EncryptedAuthData [in, out]

On input, a  pointer to the encrypted credential structure to be decrypted. On output, a pointer to the decrypted credential structure.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.

