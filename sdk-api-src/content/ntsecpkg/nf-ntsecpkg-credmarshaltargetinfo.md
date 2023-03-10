---
UID: NF:ntsecpkg.CredMarshalTargetInfo
title: CredMarshalTargetInfo function (ntsecpkg.h)
description: Serializes the specified target into an array of byte values.
helpviewer_keywords: ["CredMarshalTargetInfo","CredMarshalTargetInfo function [Security]","ntsecpkg/CredMarshalTargetInfo","security.credmarshaltargetinfo"]
old-location: security\credmarshaltargetinfo.htm
tech.root: security
ms.assetid: 1e50a135-e8b3-4aa6-a3b0-f4b1490310e5
ms.date: 12/05/2018
ms.keywords: CredMarshalTargetInfo, CredMarshalTargetInfo function [Security], ntsecpkg/CredMarshalTargetInfo, security.credmarshaltargetinfo
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredMarshalTargetInfo
 - ntsecpkg/CredMarshalTargetInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - CredMarshalTargetInfo
---

# CredMarshalTargetInfo function


## -description

Serializes the specified target into an array of byte values.

## -parameters

### -param InTargetInfo [in]

A pointer to a <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> version of the <a href="/windows/desktop/api/wincred/ns-wincred-credential_target_informationa">CREDENTIAL_TARGET_INFORMATION</a> structure that specifies the target to serialize.

### -param Buffer [out]

The serialized array of byte values that represents the target specified by the <i>InTargetInfo</i> parameter.

### -param BufferSize

The size, in bytes, of the <i>Buffer</i> array.

## -returns

If the function succeeds, it returns <b>STATUS_SUCCESS</b>.

If the function fails, it returns an error code that indicates the reason it failed.