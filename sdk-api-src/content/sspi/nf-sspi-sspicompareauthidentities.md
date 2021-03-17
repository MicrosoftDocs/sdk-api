---
UID: NF:sspi.SspiCompareAuthIdentities
title: SspiCompareAuthIdentities function (sspi.h)
description: Compares the two specified credentials.
helpviewer_keywords: ["SspiCompareAuthIdentities","SspiCompareAuthIdentities function [Security]","security.sspicompareauthidentities","sspi/SspiCompareAuthIdentities"]
old-location: security\sspicompareauthidentities.htm
tech.root: security
ms.assetid: d2c4f363-3d86-48f0-bae1-4f9240d68bab
ms.date: 12/05/2018
ms.keywords: SspiCompareAuthIdentities, SspiCompareAuthIdentities function [Security], security.sspicompareauthidentities, sspi/SspiCompareAuthIdentities
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
 - SspiCompareAuthIdentities
 - sspi/SspiCompareAuthIdentities
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
 - SspiCompareAuthIdentities
---

# SspiCompareAuthIdentities function


## -description

Compares the two specified credentials.

## -parameters

### -param AuthIdentity1 [in]

A pointer to an opaque structure that specifies the first credential to compare.

### -param AuthIdentity2 [in]

A pointer to an opaque structure that specifies the second credential to compare.

### -param SameSuppliedUser [out]

<b>TRUE</b> if the user account specified by the <i>AuthIdentity1</i> parameter is the same as the user account specified by the <i>AuthIdentity2</i> parameter; otherwise, <b>FALSE</b>.

### -param SameSuppliedIdentity [out]

<b>TRUE</b> if the identity specified by the <i>AuthIdentity1</i> parameter is the same as the identity specified by the <i>AuthIdentity2</i> parameter; otherwise, <b>FALSE</b>.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.

