---
UID: NF:sspi.SspiFreeAuthIdentity
title: SspiFreeAuthIdentity function (sspi.h)
description: Frees the memory allocated for the specified identity structure.
helpviewer_keywords: ["SspiFreeAuthIdentity","SspiFreeAuthIdentity function [Security]","security.sspifreeauthidentity","sspi/SspiFreeAuthIdentity"]
old-location: security\sspifreeauthidentity.htm
tech.root: security
ms.assetid: 6199f66e-7adb-4bb9-8e77-a735e31dd5f6
ms.date: 12/05/2018
ms.keywords: SspiFreeAuthIdentity, SspiFreeAuthIdentity function [Security], security.sspifreeauthidentity, sspi/SspiFreeAuthIdentity
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
 - SspiFreeAuthIdentity
 - sspi/SspiFreeAuthIdentity
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
 - SspiFreeAuthIdentity
---

# SspiFreeAuthIdentity function


## -description

Frees the memory allocated for the specified identity structure.

## -parameters

### -param AuthData [in]

The identity structure to free.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.

