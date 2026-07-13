---
UID: NF:dxcapi.IDxcContainerReflection.FindFirstPartKind
tech.root: direct3dhlsl
title: IDxcContainerReflection::FindFirstPartKind
ms.date: 04/05/2023
targetos: Windows
description: Retrieves the index of the first part that has the specified kind.
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
 - IDxcContainerReflection::FindFirstPartKind
f1_keywords:
 - IDxcContainerReflection::FindFirstPartKind
 - dxcapi/IDxcContainerReflection::FindFirstPartKind
dev_langs:
 - c++
helpviewer_keywords:
 - FindFirstPartKind
---

## -description

Retrieves the index of the first part that has the specified kind.

## -parameters

### -param kind

The kind to search for.

### -param pResult

A pointer to the variable in which to receive the index of the matching part.

## -returns

**S_OK** on success, or **E_NOT_VALID_STATE** if a container has not been loaded by using [Load](./nf-dxcapi-idxccontainerreflection-load.md), or **HRESULT_FROM_WIN32(ERROR_NOT_FOUND)** if there's no part with the specified kind, or another standard **HRESULT** error code.

## -remarks

## -see-also
