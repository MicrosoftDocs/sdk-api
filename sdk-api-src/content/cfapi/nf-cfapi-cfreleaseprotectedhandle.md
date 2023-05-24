---
UID: NF:cfapi.CfReleaseProtectedHandle
title: CfReleaseProtectedHandle function (cfapi.h)
description: Releases a protected handle referenced by CfReferenceProtectedHandle.
helpviewer_keywords: ["CfReleaseProtectedHandle","CfReleaseProtectedHandle function","cfapi/CfReleaseProtectedHandle","cloudApi.cfreleaseprotectedhandle"]
old-location: cloudapi\cfreleaseprotectedhandle.htm
tech.root: cloudapi
ms.assetid: BB63C5EE-92D7-4051-8198-09F50BBC75C5
ms.date: 03/30/2023
ms.keywords: CfReleaseProtectedHandle, CfReleaseProtectedHandle function, cfapi/CfReleaseProtectedHandle, cloudApi.cfreleaseprotectedhandle
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfReleaseProtectedHandle
 - cfapi/CfReleaseProtectedHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfReleaseProtectedHandle
---

# CfReleaseProtectedHandle function

## -description

Releases a protected handle referenced by [CfReferenceProtectedHandle](nf-cfapi-cfreferenceprotectedhandle.md).

## -parameters

### -param ProtectedHandle [in]

The protected handle to be released.

## -see-also

[CfReferenceProtectedHandle](nf-cfapi-cfreferenceprotectedhandle.md)
