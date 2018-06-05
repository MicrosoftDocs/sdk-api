---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_FILE_INFO
title: "_D3D10_SHADER_DEBUG_FILE_INFO"
author: windows-sdk-content
description: Describes files included by a shader.
old-location: direct3d10\d3d10_shader_debug_file_info.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_file_info.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: D3D10_SHADER_DEBUG_FILE_INFO, D3D10_SHADER_DEBUG_FILE_INFO structure [Direct3D 10], _D3D10_SHADER_DEBUG_FILE_INFO, ac4c1ede-a189-df0e-6b8f-755a37f8de3d, d3d10_1shader/D3D10_SHADER_DEBUG_FILE_INFO, direct3d10.d3d10_shader_debug_file_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: D3D10_SHADER_DEBUG_FILE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d10_1shader.h
api_name:
-	D3D10_SHADER_DEBUG_FILE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D10_SHADER_DEBUG_FILE_INFO structure


## -description


Describes files included by a shader.


## -struct-fields




### -field FileName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to the LPCSTR for the file name.


### -field FileNameLen

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Length of the file name.


### -field FileData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to the file data.


### -field FileLen

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Length of the file.


## -remarks



The <b>D3D10_SHADER_DEBUG_FILE_INFO</b> structure is used with the <a href="https://msdn.microsoft.com/b1b4201a-5bfb-4fce-ba51-64f7da9531bc">D3D10_SHADER_DEBUG_INFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/b36309e0-1c44-42d9-adcf-33acd753438c">Shader Structures</a>
 

 

