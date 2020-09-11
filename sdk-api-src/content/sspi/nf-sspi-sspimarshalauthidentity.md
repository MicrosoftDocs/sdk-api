---
UID: NF:sspi.SspiMarshalAuthIdentity
title: SspiMarshalAuthIdentity function (sspi.h)
description: Serializes the specified identity structure into a byte array.
helpviewer_keywords: ["SspiMarshalAuthIdentity","SspiMarshalAuthIdentity function [Security]","security.sspimarshalauthidentity","sspi/SspiMarshalAuthIdentity"]
old-location: security\sspimarshalauthidentity.htm
tech.root: security
ms.assetid: e43135ad-7fcd-4da6-a4e4-c91c41eeb865
ms.date: 12/05/2018
ms.keywords: SspiMarshalAuthIdentity, SspiMarshalAuthIdentity function [Security], security.sspimarshalauthidentity, sspi/SspiMarshalAuthIdentity
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
 - SspiMarshalAuthIdentity
 - sspi/SspiMarshalAuthIdentity
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
 - SspiMarshalAuthIdentity
---

# SspiMarshalAuthIdentity function


## -description

Serializes the specified identity structure into a byte array.

## -parameters

### -param AuthIdentity [in]

The identity structure to serialize.

### -param AuthIdentityLength [out]

The length, in bytes, of the <i>AuthIdentityByteArray</i> array.

### -param AuthIdentityByteArray [out]

A pointer to an array of byte values that represents the identity specified by the <i>AuthIdentity</i> parameter.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.

