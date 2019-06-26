---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_FILE_INFO
title: D3D10_SHADER_DEBUG_FILE_INFO (d3d10_1shader.h)
author: windows-sdk-content
description: Describes files included by a shader.
old-location: direct3d10\d3d10_shader_debug_file_info.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_file_info.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D10_SHADER_DEBUG_FILE_INFO, D3D10_SHADER_DEBUG_FILE_INFO structure [Direct3D 10], ac4c1ede-a189-df0e-6b8f-755a37f8de3d, d3d10_1shader/D3D10_SHADER_DEBUG_FILE_INFO, direct3d10.d3d10_shader_debug_file_info
ms.topic: struct
f1_keywords: 
 - "d3d10_1shader/D3D10_SHADER_DEBUG_FILE_INFO"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10_1shader.h
api_name:
 - D3D10_SHADER_DEBUG_FILE_INFO
product: Windows
targetos: Windows
req.typenames: D3D10_SHADER_DEBUG_FILE_INFO
req.redist: 
ms.custom: 19H1
---

# D3D10_SHADER_DEBUG_FILE_INFO structure


## -description


Describes files included by a shader.


## -struct-fields




### -field FileName

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to the LPCSTR for the file name.


### -field FileNameLen

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Length of the file name.


### -field FileData

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to the file data.


### -field FileLen

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Length of the file.


## -remarks



The <b>D3D10_SHADER_DEBUG_FILE_INFO</b> structure is used with the <a href="https://docs.microsoft.com/windows/desktop/api/d3d10_1shader/ns-d3d10_1shader-_d3d10_shader_debug_info">D3D10_SHADER_DEBUG_INFO</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>
 

 

