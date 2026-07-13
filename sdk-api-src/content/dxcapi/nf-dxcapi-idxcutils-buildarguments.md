---
UID: NF:dxcapi.IDxcUtils.BuildArguments
tech.root: direct3dhlsl
title: IDxcUtils::BuildArguments
ms.date: 04/05/2023
targetos: Windows
description: Build arguments that can be passed to the [Compile](./nf-dxcapi-idxccompiler3-compile.md) method.
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
 - IDxcUtils::BuildArguments
f1_keywords:
 - IDxcUtils::BuildArguments
 - dxcapi/IDxcUtils::BuildArguments
dev_langs:
 - c++
helpviewer_keywords:
 - BuildArguments
---

## -description

Build arguments that can be passed to the [Compile](./nf-dxcapi-idxccompiler3-compile.md) method.

## -parameters

### -param pSourceName

An optional file name. Used in errors and include handlers.

### -param pEntryPoint

Entry point name (`-E`).

### -param pTargetProfile

Shader profile to compile (`-T`).

### -param pArguments

An array of pointers to arguments.

### -param argCount

The number of arguments.

### -param pDefines

An array of defines.

### -param defineCount

The number of defines.

### -param ppArgs

Arguments that you can use with the [IDxcCompiler3::Compile](./nf-dxcapi-idxccompiler3-compile.md) method.

## -returns

## -remarks

## -see-also
