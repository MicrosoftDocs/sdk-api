---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_TOKEN_INFO
title: "_D3D10_SHADER_DEBUG_TOKEN_INFO"
author: windows-sdk-content
description: Gives the source location for a shader element.
old-location: direct3d10\d3d10_shader_debug_token_info.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_token_info.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: D3D10_SHADER_DEBUG_TOKEN_INFO, D3D10_SHADER_DEBUG_TOKEN_INFO structure [Direct3D 10], _D3D10_SHADER_DEBUG_TOKEN_INFO, bc17063b-6965-506e-6465-5f361287445e, d3d10_1shader/D3D10_SHADER_DEBUG_TOKEN_INFO, direct3d10.d3d10_shader_debug_token_info
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
req.typenames: D3D10_SHADER_DEBUG_TOKEN_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d10_1shader.h
api_name:
-	D3D10_SHADER_DEBUG_TOKEN_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D10_SHADER_DEBUG_TOKEN_INFO structure


## -description


Gives the source location for a shader element.


## -struct-fields




### -field File

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset into file list.


### -field Line

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Line number.


### -field Column

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Column number.


### -field TokenLength

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Length of the token.


### -field TokenId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to LPCSTR of length <b>TokenLength</b> in string datastore.


## -see-also




<a href="https://msdn.microsoft.com/b36309e0-1c44-42d9-adcf-33acd753438c">Shader Structures</a>
 

 

