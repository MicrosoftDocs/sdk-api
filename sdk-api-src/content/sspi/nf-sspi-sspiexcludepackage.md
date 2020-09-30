---
UID: NF:sspi.SspiExcludePackage
title: SspiExcludePackage function (sspi.h)
description: Creates a new identity structure that is a copy of the specified identity structure modified to exclude the specified security support provider (SSP).
helpviewer_keywords: ["SspiExcludePackage","SspiExcludePackage function [Security]","security.sspiexcludepackage","sspi/SspiExcludePackage"]
old-location: security\sspiexcludepackage.htm
tech.root: security
ms.assetid: 2f85bb13-b72a-4c26-a328-9424a33a63b8
ms.date: 12/05/2018
ms.keywords: SspiExcludePackage, SspiExcludePackage function [Security], security.sspiexcludepackage, sspi/SspiExcludePackage
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
 - SspiExcludePackage
 - sspi/SspiExcludePackage
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
 - SspiExcludePackage
---

# SspiExcludePackage function


## -description

Creates a new identity structure that is a copy of  the specified identity structure modified to exclude the specified <a href="/windows/desktop/SecGloss/s-gly">security support provider</a> (SSP).

## -parameters

### -param AuthIdentity [in]

The identity structure to modify.

### -param pszPackageName [in]

The SSP to exclude.

### -param ppNewAuthIdentity [out]

The modified identity structure.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.