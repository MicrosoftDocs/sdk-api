---
UID: NF:sspi.SspiPrepareForCredRead
title: SspiPrepareForCredRead function (sspi.h)
description: Generates a target name and credential type from the specified identity structure.
helpviewer_keywords: ["SspiPrepareForCredRead","SspiPrepareForCredRead function [Security]","security.sspiprepareforcredread","sspi/SspiPrepareForCredRead"]
old-location: security\sspiprepareforcredread.htm
tech.root: security
ms.assetid: f473fd7a-5c0f-4a77-829b-28a82ad0d28d
ms.date: 12/05/2018
ms.keywords: SspiPrepareForCredRead, SspiPrepareForCredRead function [Security], security.sspiprepareforcredread, sspi/SspiPrepareForCredRead
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
 - SspiPrepareForCredRead
 - sspi/SspiPrepareForCredRead
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
 - SspiPrepareForCredRead
---

# SspiPrepareForCredRead function


## -description

Generates a target name and credential type from the specified identity structure.

The values that this function generates can be passed as the values of the <i>TargetName</i> and <i>Type</i> parameters in a call to the <a href="/windows/desktop/api/wincred/nf-wincred-credreada">CredRead</a> function.

## -parameters

### -param AuthIdentity [in]

The identity structure from which to generate the credentials to be passed to the <a href="/windows/desktop/api/wincred/nf-wincred-credreada">CredRead</a> function.

### -param pszTargetName [in]

A target name that can be modified by this function depending on the value of the <i>AuthIdentity</i> parameter.

### -param pCredmanCredentialType [out]

The credential type to pass to the <a href="/windows/desktop/api/wincred/nf-wincred-credreada">CredRead</a> function.

### -param ppszCredmanTargetName [out]

The target name to pass to the <a href="/windows/desktop/api/wincred/nf-wincred-credreada">CredRead</a> function.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.