---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_SCOPE_INFO
title: "_D3D10_SHADER_DEBUG_SCOPE_INFO"
author: windows-sdk-content
description: Contains scope data that maps variable names to debug variables.
old-location: direct3d10\d3d10_shader_debug_scope_info.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_scope_info.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 98b3a0e8-be0d-c4db-defc-df94817adf46, D3D10_SHADER_DEBUG_SCOPE_INFO, D3D10_SHADER_DEBUG_SCOPE_INFO structure [Direct3D 10], _D3D10_SHADER_DEBUG_SCOPE_INFO, d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_INFO, direct3d10.d3d10_shader_debug_scope_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10_1shader.h
req.include-header: D3D10Shader.h
req.redist: 
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
tech.root: 
req.typenames: D3D10_SHADER_DEBUG_SCOPE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10_1shader.h
api_name:
 - D3D10_SHADER_DEBUG_SCOPE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D10_SHADER_DEBUG_SCOPE_INFO structure


## -description


Contains scope data that maps variable names to debug variables.


## -struct-fields




### -field ScopeType

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172426(v=VS.85).aspx">D3D10_SHADER_DEBUG_SCOPETYPE</a></b>

Specifies the scope type.


### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to the name of scope in the strings list.


### -field uNameLen

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Length of the string pointed to by <b>Name</b>.


### -field uVariables

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of variables.


### -field VariableData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset an array of UINT values with <b>uVariables</b> members contianing the scope variable list.


## -remarks



The <b>D3D10_SHADER_DEBUG_SCOPE_INFO</b> structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb172420(v=VS.85).aspx">D3D10_SHADER_DEBUG_INFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205159(v=VS.85).aspx">Shader Structures</a>
 

 

