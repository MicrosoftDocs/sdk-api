---
UID: NF:dxcapi.IDxcVersionInfo2.GetCommitInfo
tech.root: direct3dhlsl
title: IDxcVersionInfo2::GetCommitInfo
ms.date: 04/05/2023
targetos: Windows
description: TBD
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: dxcapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dxcapi.h
api_name:
 - IDxcVersionInfo2::GetCommitInfo
f1_keywords:
 - IDxcVersionInfo2::GetCommitInfo
 - dxcapi/IDxcVersionInfo2::GetCommitInfo
dev_langs:
 - c++
helpviewer_keywords:
 - GetCommitInfo
---

## -description

## -parameters

### -param pCommitCount

The total number of commits.

### -param pCommitHash

The SHA of the latest commit. You must free this memory by using [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

## -returns

## -remarks

## -see-also
