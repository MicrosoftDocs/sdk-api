---
UID: NF:dxcapi.IDxcCompiler3.Compile
tech.root: direct3dhlsl
title: IDxcCompiler3::Compile
ms.date: 04/05/2023
targetos: Windows
description: Compile a single entry point to the target shader model, or compile a library to a library target, or compile a root signature, or preprocess HLSL source.
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
 - IDxcCompiler3::Compile
f1_keywords:
 - IDxcCompiler3::Compile
 - dxcapi/IDxcCompiler3::Compile
dev_langs:
 - c++
helpviewer_keywords:
 - Compile
---

## -description

Compile a shader. Depending on the arguments, you can use this method to:

* Compile a single entry point to the target shader model
* Compile a library to a library target (`-T lib_*`)
* Compile a root signature (`-T rootsig_*`),
* Preprocess HLSL source (`-P`)

You can use [IDxcUtils::BuildArguments](./nf-dxcapi-idxcutils-buildarguments) to assist in building the *pArguments* and *argCount* arguments.

## -parameters

### -param pSource

The source text to compile.

### -param pArguments

An array of pointers to arguments.

### -param argCount

The number of arguments.

### -param pIncludeHandler

An optional user-provided interface to handle `#include` directives.

### -param riid

The interface ID for the result.

### -param ppResult

An [IDxcResult](./ns-dxcapi-idxcresult.md) representing the compiler output status, buffer, and errors.

## -returns

## -remarks

## -see-also
