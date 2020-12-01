---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_FILE_INFO
title: D3D10_SHADER_DEBUG_FILE_INFO (d3d10_1shader.h)
description: Describes files included by a shader.
helpviewer_keywords: ["D3D10_SHADER_DEBUG_FILE_INFO","D3D10_SHADER_DEBUG_FILE_INFO structure [Direct3D 10]","ac4c1ede-a189-df0e-6b8f-755a37f8de3d","d3d10_1shader/D3D10_SHADER_DEBUG_FILE_INFO","direct3d10.d3d10_shader_debug_file_info"]
old-location: direct3d10\d3d10_shader_debug_file_info.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_file_info.htm
ms.date: 12/05/2018
ms.keywords: D3D10_SHADER_DEBUG_FILE_INFO, D3D10_SHADER_DEBUG_FILE_INFO structure [Direct3D 10], ac4c1ede-a189-df0e-6b8f-755a37f8de3d, d3d10_1shader/D3D10_SHADER_DEBUG_FILE_INFO, direct3d10.d3d10_shader_debug_file_info
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
req.typenames: D3D10_SHADER_DEBUG_FILE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_DEBUG_FILE_INFO
 - d3d10_1shader/_D3D10_SHADER_DEBUG_FILE_INFO
 - D3D10_SHADER_DEBUG_FILE_INFO
 - d3d10_1shader/D3D10_SHADER_DEBUG_FILE_INFO
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
 - D3D10_SHADER_DEBUG_FILE_INFO
---

# D3D10_SHADER_DEBUG_FILE_INFO structure


## -description

Describes files included by a shader.

## -struct-fields

### -field FileName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to the LPCSTR for the file name.

### -field FileNameLen

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Length of the file name.

### -field FileData

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to the file data.

### -field FileLen

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Length of the file.

## -remarks

The <b>D3D10_SHADER_DEBUG_FILE_INFO</b> structure is used with the <a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_info">D3D10_SHADER_DEBUG_INFO</a> structure.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>