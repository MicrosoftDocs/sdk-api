---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_TOKEN_INFO
title: D3D10_SHADER_DEBUG_TOKEN_INFO (d3d10_1shader.h)
description: Gives the source location for a shader element.
helpviewer_keywords: ["D3D10_SHADER_DEBUG_TOKEN_INFO","D3D10_SHADER_DEBUG_TOKEN_INFO structure [Direct3D 10]","bc17063b-6965-506e-6465-5f361287445e","d3d10_1shader/D3D10_SHADER_DEBUG_TOKEN_INFO","direct3d10.d3d10_shader_debug_token_info"]
old-location: direct3d10\d3d10_shader_debug_token_info.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_token_info.htm
ms.date: 12/05/2018
ms.keywords: D3D10_SHADER_DEBUG_TOKEN_INFO, D3D10_SHADER_DEBUG_TOKEN_INFO structure [Direct3D 10], bc17063b-6965-506e-6465-5f361287445e, d3d10_1shader/D3D10_SHADER_DEBUG_TOKEN_INFO, direct3d10.d3d10_shader_debug_token_info
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
req.typenames: D3D10_SHADER_DEBUG_TOKEN_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_DEBUG_TOKEN_INFO
 - d3d10_1shader/_D3D10_SHADER_DEBUG_TOKEN_INFO
 - D3D10_SHADER_DEBUG_TOKEN_INFO
 - d3d10_1shader/D3D10_SHADER_DEBUG_TOKEN_INFO
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
 - D3D10_SHADER_DEBUG_TOKEN_INFO
---

# D3D10_SHADER_DEBUG_TOKEN_INFO structure


## -description

Gives the source location for a shader element.

## -struct-fields

### -field File

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset into file list.

### -field Line

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Line number.

### -field Column

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Column number.

### -field TokenLength

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Length of the token.

### -field TokenId

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to LPCSTR of length <b>TokenLength</b> in string datastore.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>