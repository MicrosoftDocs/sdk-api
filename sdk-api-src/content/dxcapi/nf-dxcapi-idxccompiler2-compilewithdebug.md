---
UID: NF:dxcapi.IDxcCompiler2.CompileWithDebug
tech.root: direct3dhlsl
title: IDxcCompiler2::CompileWithDebug
ms.date: 04/05/2023
targetos: Windows
description: Compile a single entry point to the target shader model with debug information. **IDxcCompiler::CompileWithDebug** is deprecated; use [IDxcCompiler3::Compile](./nf-dxcapi-idxccompiler3-disassemble.md) instead.
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
 - IDxcCompiler2::CompileWithDebug
f1_keywords:
 - IDxcCompiler2::CompileWithDebug
 - dxcapi/IDxcCompiler2::CompileWithDebug
dev_langs:
 - c++
helpviewer_keywords:
 - CompileWithDebug
---

## -description

Compile a single entry point to the target shader model with debug information. **IDxcCompiler::CompileWithDebug** is deprecated; use [IDxcCompiler3::Compile](./nf-dxcapi-idxccompiler3-disassemble.md) instead.

## -parameters

### -param pSource

The source text to compile.

### -param pSourceName

An optional file name for *pSource*. Used in errors and include handlers.

### -param pEntryPoint

Entry point name.

### -param pTargetProfile

Shader profile to compile.

### -param pArguments

An array of pointers to arguments.

### -param argCount

The number of arguments.

### -param pDefines

An array of defines.

### -param defineCount

The number of defines.

### -param pIncludeHandler

An optional user-provided interface to handle `#include` directives.

### -param ppResult

The compiler output status, buffer, and errors.

### -param ppDebugBlobName

A suggested file name for the debug blob. You must free this memory by using [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

### -param ppDebugBlob

The debug blob.

## -returns

## -remarks

## -see-also
