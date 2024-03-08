---
UID: NF:cfapi.CfReferenceProtectedHandle
title: CfReferenceProtectedHandle function (cfapi.h)
description: Allows the caller to reference a protected handle to a Win32 handle which can be used with non-CfApi Win32 APIs.
helpviewer_keywords: ["CfReferenceProtectedHandle","CfReferenceProtectedHandle function","cfapi/CfReferenceProtectedHandle","cloudApi.cfreferenceprotectedhandle"]
old-location: cloudapi\cfreferenceprotectedhandle.htm
tech.root: cloudapi
ms.assetid: C6281FD6-3A37-4D90-9B19-03DD23949C39
ms.date: 03/30/2023
ms.keywords: CfReferenceProtectedHandle, CfReferenceProtectedHandle function, cfapi/CfReferenceProtectedHandle, cloudApi.cfreferenceprotectedhandle
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
 - CfReferenceProtectedHandle
 - cfapi/CfReferenceProtectedHandle
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
 - CfReferenceProtectedHandle
---

# CfReferenceProtectedHandle function

## -description

Allows the caller to reference a protected handle to a Win32 handle which can be used with non-CfApi Win32 APIs.

## -parameters

### -param ProtectedHandle [in]

The protected handle of a placeholder file.

## -returns

If this function succeeds, it returns `TRUE`. Otherwise, it returns `FALSE`.

## -remarks

Every **CfReferenceProtectedHandle** call must be matched  with a [CfReleaseProtectedHandle](nf-cfapi-cfreleaseprotectedhandle.md) call. It is not recommended to reference a protected handle for a long period of time, as doing so will prevent the oplock break notification from being acknowledged.

The caller should instead break up long running tasks into smaller sub-tasks and reference/release the protected handle for each sub-task.

## -see-also

[CfReleaseProtectedHandle](nf-cfapi-cfreleaseprotectedhandle.md)
