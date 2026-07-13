---
UID: NE:d3d10_1shader._D3D10_SHADER_DEBUG_SCOPETYPE
title: D3D10_SHADER_DEBUG_SCOPETYPE (d3d10_1shader.h)
description: Scope types.
helpviewer_keywords: ["D3D10_SHADER_DEBUG_SCOPETYPE","D3D10_SHADER_DEBUG_SCOPETYPE enumeration [Direct3D 10]","D3D10_SHADER_DEBUG_SCOPE_ANNOTATION","D3D10_SHADER_DEBUG_SCOPE_BLOCK","D3D10_SHADER_DEBUG_SCOPE_FORCE_DWORD","D3D10_SHADER_DEBUG_SCOPE_FORLOOP","D3D10_SHADER_DEBUG_SCOPE_FUNC_PARAMS","D3D10_SHADER_DEBUG_SCOPE_GLOBAL","D3D10_SHADER_DEBUG_SCOPE_NAMESPACE","D3D10_SHADER_DEBUG_SCOPE_STATEBLOCK","D3D10_SHADER_DEBUG_SCOPE_STRUCT","a42aff03-01b4-0000-857a-579862c3b15e","d3d10_1shader/D3D10_SHADER_DEBUG_SCOPETYPE","d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_ANNOTATION","d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_BLOCK","d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_FORCE_DWORD","d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_FORLOOP","d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_FUNC_PARAMS","d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_GLOBAL","d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_NAMESPACE","d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_STATEBLOCK","d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_STRUCT","direct3d10.d3d10_shader_debug_scopetype"]
old-location: direct3d10\d3d10_shader_debug_scopetype.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_scopetype.htm
ms.date: 12/05/2018
ms.keywords: D3D10_SHADER_DEBUG_SCOPETYPE, D3D10_SHADER_DEBUG_SCOPETYPE enumeration [Direct3D 10], D3D10_SHADER_DEBUG_SCOPE_ANNOTATION, D3D10_SHADER_DEBUG_SCOPE_BLOCK, D3D10_SHADER_DEBUG_SCOPE_FORCE_DWORD, D3D10_SHADER_DEBUG_SCOPE_FORLOOP, D3D10_SHADER_DEBUG_SCOPE_FUNC_PARAMS, D3D10_SHADER_DEBUG_SCOPE_GLOBAL, D3D10_SHADER_DEBUG_SCOPE_NAMESPACE, D3D10_SHADER_DEBUG_SCOPE_STATEBLOCK, D3D10_SHADER_DEBUG_SCOPE_STRUCT, a42aff03-01b4-0000-857a-579862c3b15e, d3d10_1shader/D3D10_SHADER_DEBUG_SCOPETYPE, d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_ANNOTATION, d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_BLOCK, d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_FORCE_DWORD, d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_FORLOOP, d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_FUNC_PARAMS, d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_GLOBAL, d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_NAMESPACE, d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_STATEBLOCK, d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_STRUCT, direct3d10.d3d10_shader_debug_scopetype
req.header: d3d10_1shader.h
req.include-header: D3D10Shader.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D10_SHADER_DEBUG_SCOPETYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_DEBUG_SCOPETYPE
 - d3d10_1shader/_D3D10_SHADER_DEBUG_SCOPETYPE
 - D3D10_SHADER_DEBUG_SCOPETYPE
 - d3d10_1shader/D3D10_SHADER_DEBUG_SCOPETYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10_1shader.h
api_name:
 - D3D10_SHADER_DEBUG_SCOPETYPE
---

# D3D10_SHADER_DEBUG_SCOPETYPE enumeration


## -description

Scope types.

## -enum-fields

### -field D3D10_SHADER_DEBUG_SCOPE_GLOBAL

Global scope.

### -field D3D10_SHADER_DEBUG_SCOPE_BLOCK

Block scope.

### -field D3D10_SHADER_DEBUG_SCOPE_FORLOOP

For loop scope.

### -field D3D10_SHADER_DEBUG_SCOPE_STRUCT

Structure scope.

### -field D3D10_SHADER_DEBUG_SCOPE_FUNC_PARAMS

Function parameter scope.

### -field D3D10_SHADER_DEBUG_SCOPE_STATEBLOCK

State block scope.

### -field D3D10_SHADER_DEBUG_SCOPE_NAMESPACE

Name space scope.

### -field D3D10_SHADER_DEBUG_SCOPE_ANNOTATION

Annotation scope.

### -field D3D10_SHADER_DEBUG_SCOPE_FORCE_DWORD:0x7fffffff

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.

## -remarks

The <b>D3D10_SHADER_DEBUG_SCOPETYPE</b> enumeration is used to specify scope type in the <a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_scope_info">D3D10_SHADER_DEBUG_SCOPE_INFO</a> structure.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-enums">Shader Enumerations</a>
