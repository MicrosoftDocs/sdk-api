---
UID: NF:d3d10.ID3D10Device.CreateVertexShader
title: ID3D10Device::CreateVertexShader
author: windows-sdk-content
description: Create a vertex-shader object from a compiled shader.
old-location: direct3d10\id3d10device_createvertexshader.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createvertexshader.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 85865e55-ec77-0246-1f72-283d1333b4e7, CreateVertexShader, CreateVertexShader method [Direct3D 10], CreateVertexShader method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateVertexShader method, ID3D10Device.CreateVertexShader, ID3D10Device::CreateVertexShader, d3d10/ID3D10Device::CreateVertexShader, direct3d10.id3d10device_createvertexshader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
req.include-header: 
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreateVertexShader
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::CreateVertexShader


## -description


Create a vertex-shader object from a compiled shader.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader. To get this pointer see <a href="https://msdn.microsoft.com/en-us/library/Bb509703(v=VS.85).aspx">Getting a Pointer to a Compiled Shader</a>.


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Size of the compiled vertex shader.


### -param ppVertexShader [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173875(v=VS.85).aspx">ID3D10VertexShader</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb173875(v=VS.85).aspx">ID3D10VertexShader Interface</a>. If this is <b>NULL</b>, all other parameters will be validated, and if all parameters pass validation this API will return S_FALSE instead of S_OK.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

