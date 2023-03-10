---
UID: NF:sspi.SspiZeroAuthIdentity
title: SspiZeroAuthIdentity function (sspi.h)
description: Fills the block of memory associated with the specified identity structure with zeros.
helpviewer_keywords: ["SspiZeroAuthIdentity","SspiZeroAuthIdentity function [Security]","security.sspizeroauthidentity","sspi/SspiZeroAuthIdentity"]
old-location: security\sspizeroauthidentity.htm
tech.root: security
ms.assetid: 50b1f24a-c802-4691-a450-316cb31bf44d
ms.date: 12/05/2018
ms.keywords: SspiZeroAuthIdentity, SspiZeroAuthIdentity function [Security], security.sspizeroauthidentity, sspi/SspiZeroAuthIdentity
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
 - SspiZeroAuthIdentity
 - sspi/SspiZeroAuthIdentity
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
 - SspiZeroAuthIdentity
---

# SspiZeroAuthIdentity function


## -description

Fills the block of memory associated with the specified identity structure with zeros.

## -parameters

### -param AuthData [in]

The identity structure to fill with zeros.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.

