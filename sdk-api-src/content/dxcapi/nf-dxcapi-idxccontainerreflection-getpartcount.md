---
UID: NF:dxcapi.IDxcContainerReflection.GetPartCount
tech.root: direct3dhlsl
title: IDxcContainerReflection::GetPartCount
ms.date: 04/05/2023
targetos: Windows
description: Retrieves the number of parts in the container.
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
 - IDxcContainerReflection::GetPartCount
f1_keywords:
 - IDxcContainerReflection::GetPartCount
 - dxcapi/IDxcContainerReflection::GetPartCount
dev_langs:
 - c++
helpviewer_keywords:
 - GetPartCount
---

## -description

Retrieves the number of parts in the container.

## -parameters

### -param pResult

A pointer to the variable in which to receive the result.

## -returns

**S_OK** on success, or **E_NOT_VALID_STATE** if a container has not been loaded by using [Load](./nf-dxcapi-idxccontainerreflection-load.md), or another standard **HRESULT** error code.

## -remarks

## -see-also
