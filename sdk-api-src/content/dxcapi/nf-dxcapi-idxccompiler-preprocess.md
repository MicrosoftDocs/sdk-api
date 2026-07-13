---
UID: NF:dxcapi.IDxcCompiler.Preprocess
tech.root: direct3dhlsl
title: IDxcCompiler::Preprocess
ms.date: 04/05/2023
targetos: Windows
description: Preprocess source text.
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
 - IDxcCompiler::Preprocess
f1_keywords:
 - IDxcCompiler::Preprocess
 - dxcapi/IDxcCompiler::Preprocess
dev_langs:
 - c++
helpviewer_keywords:
 - Preprocess
---

## -description

Preprocess source text. **IDxcCompiler::Preprocess** is deprecated; use [IDxcCompiler3::Compile](./nf-dxcapi-idxccompiler3-compile.md) with the `-P` argument instead.

## -parameters

### -param pSource

The source text to preprocess.

### -param pSourceName

An optional file name for *pSource*. Used in errors and include handlers.

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

The preprocessor output status, buffer, and errors.

## -returns

## -remarks

## -see-also
