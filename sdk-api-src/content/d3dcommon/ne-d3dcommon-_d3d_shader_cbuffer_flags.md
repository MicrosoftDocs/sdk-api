---
UID: NE:d3dcommon._D3D_SHADER_CBUFFER_FLAGS
title: "_D3D_SHADER_CBUFFER_FLAGS"
author: windows-sdk-content
description: Values that identify the indended use of a constant-data buffer.
old-location: direct3d11\d3d_shader_cbuffer_flags.htm
tech.root: direct3d11
ms.assetid: f641b3ec-5492-4835-9cf6-e41447e4b6b6
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: D3D10_CBF_USERPACKED, D3D_CBF_FORCE_DWORD, D3D_CBF_USERPACKED, D3D_SHADER_CBUFFER_FLAGS, D3D_SHADER_CBUFFER_FLAGS enumeration [Direct3D 11], _D3D_SHADER_CBUFFER_FLAGS, d3dcommon/D3D10_CBF_USERPACKED, d3dcommon/D3D_CBF_FORCE_DWORD, d3dcommon/D3D_CBF_USERPACKED, d3dcommon/D3D_SHADER_CBUFFER_FLAGS, direct3d11.d3d_shader_cbuffer_flags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3dcommon.h
req.include-header: 
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
 - D3DCommon.h
api_name:
 - D3D_SHADER_CBUFFER_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D_SHADER_CBUFFER_FLAGS
req.redist: 
---

# _D3D_SHADER_CBUFFER_FLAGS enumeration


## -description


Values that identify the indended use of a constant-data buffer.


## -enum-fields




### -field D3D_CBF_USERPACKED

Bind the constant buffer to an input slot defined in HLSL code (instead of letting the compiler choose the input slot).


### -field D3D10_CBF_USERPACKED

Bind the constant buffer to an input slot defined in HLSL code (instead of letting the compiler choose the input slot).


### -field D3D_CBF_FORCE_DWORD

This value is not used by a programmer; it exists to force the enumeration to compile to 32 bits.


## -remarks



<b>D3D_SHADER_CBUFFER_FLAGS</b>-typed values are specified in the <b>uFlags</b> member of the <a href="https://msdn.microsoft.com/deea8d5d-2431-4449-baa8-68a4b9b30307">D3D11_SHADER_BUFFER_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

