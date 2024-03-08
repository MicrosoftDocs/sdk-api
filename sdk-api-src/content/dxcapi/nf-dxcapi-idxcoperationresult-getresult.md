---
UID: NF:dxcapi.IDxcOperationResult.GetResult
tech.root: direct3dhlsl
title: IDxcOperationResult::GetResult
ms.date: 04/05/2023
targetos: Windows
description: Retrieves the primary output of the operation.
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
 - IDxcOperationResult::GetResult
f1_keywords:
 - IDxcOperationResult::GetResult
 - dxcapi/IDxcOperationResult::GetResult
dev_langs:
 - c++
helpviewer_keywords:
 - GetResult
---

## -description

Retrieves the primary output of the operation. This corresponds to:

* [DXC_OUT_OBJECT](./ne-dxcapi-dxc_out_kind.md). **Compile** with shader or library target.
* **DXC_OUT_DISASSEMBLY**. **Disassemble**.
* **DXC_OUT_HLSL**. **Compile** with `-P`.
* **DXC_OUT_ROOT_SIGNATURE**. **Compile** with with `rootsig_* target`.

## -parameters

### -param ppResult

The primary output of the operation.

## -returns

## -remarks

## -see-also
