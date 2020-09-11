---
UID: NF:sspi.SspiValidateAuthIdentity
title: SspiValidateAuthIdentity function (sspi.h)
description: Indicates whether the specified identity structure is valid.
helpviewer_keywords: ["SspiValidateAuthIdentity","SspiValidateAuthIdentity function [Security]","security.sspivalidateauthidentity","sspi/SspiValidateAuthIdentity"]
old-location: security\sspivalidateauthidentity.htm
tech.root: security
ms.assetid: 82733abd-d984-4902-b6e4-c3809171ad51
ms.date: 12/05/2018
ms.keywords: SspiValidateAuthIdentity, SspiValidateAuthIdentity function [Security], security.sspivalidateauthidentity, sspi/SspiValidateAuthIdentity
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
 - SspiValidateAuthIdentity
 - sspi/SspiValidateAuthIdentity
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
 - SspiValidateAuthIdentity
---

# SspiValidateAuthIdentity function


## -description

Indicates whether the specified identity structure is valid.

## -parameters

### -param AuthData [in]

The identity structure to test.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>, which indicates that the identity structure specified by the <i>AuthData</i> parameter is valid.

If the function fails, it returns a nonzero error code that indicates that the identity structure specified by the <i>AuthData</i> parameter is not valid.

