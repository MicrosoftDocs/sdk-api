---
UID: NF:sspi.SspiEncryptAuthIdentity
title: SspiEncryptAuthIdentity function (sspi.h)
description: Encrypts the specified identity structure.
helpviewer_keywords: ["SspiEncryptAuthIdentity","SspiEncryptAuthIdentity function [Security]","security.sspiencryptauthidentity","sspi/SspiEncryptAuthIdentity"]
old-location: security\sspiencryptauthidentity.htm
tech.root: security
ms.assetid: 4460f7ec-35fd-4ad1-8c20-dda9f4d3477a
ms.date: 12/05/2018
ms.keywords: SspiEncryptAuthIdentity, SspiEncryptAuthIdentity function [Security], security.sspiencryptauthidentity, sspi/SspiEncryptAuthIdentity
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
 - SspiEncryptAuthIdentity
 - sspi/SspiEncryptAuthIdentity
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
 - SspiEncryptAuthIdentity
---

# SspiEncryptAuthIdentity function


## -description

Encrypts the specified identity structure.

## -parameters

### -param AuthData [in, out]

On input, the identity structure to encrypt. On output, the encrypted identity structure.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.

