---
UID: NF:ncrypt.NCryptCreateClaim
title: NCryptCreateClaim function (ncrypt.h)
description: Creates a key attestation claim.
helpviewer_keywords: ["NCryptCreateClaim","NCryptCreateClaim function [Security]","ncrypt/NCryptCreateClaim","security.ncryptcreateclaim"]
old-location: security\ncryptcreateclaim.htm
tech.root: security
ms.assetid: EBEE3A67-0693-4B85-88B1-580CB2152703
ms.date: 12/05/2018
ms.keywords: NCryptCreateClaim, NCryptCreateClaim function [Security], ncrypt/NCryptCreateClaim, security.ncryptcreateclaim
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptCreateClaim
 - ncrypt/NCryptCreateClaim
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ncrypt.dll
api_name:
 - NCryptCreateClaim
---

# NCryptCreateClaim function


## -description



Creates a key attestation claim.

## -parameters

### -param hSubjectKey [in]

The subject key handle that the claim is created for.

### -param hAuthorityKey [in, optional]

The authority key handle that the claim is based on.

### -param dwClaimType [in]

The type of claim.

### -param pParameterList [in, optional]

An optional parameter list.

### -param pbClaimBlob [out]

Output of the created claim blob.

### -param cbClaimBlob [in]

### -param pcbResult [out]

The output of the created claim blob.

### -param dwFlags [in]

As of Windows 10, no  flags are defined. This parameter should be set to 0.

## -returns

Returns a status code that indicates the success or failure of the function.
