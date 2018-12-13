---
UID: NF:d3d10.ID3D10Device.CreateGeometryShader
title: ID3D10Device::CreateGeometryShader
author: windows-sdk-content
description: Create a geometry shader.
old-location: direct3d10\id3d10device_creategeometryshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_creategeometryshader.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 95304c4b-5772-79d5-e004-826cea33692b, CreateGeometryShader, CreateGeometryShader method [Direct3D 10], CreateGeometryShader method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateGeometryShader method, ID3D10Device.CreateGeometryShader, ID3D10Device::CreateGeometryShader, d3d10/ID3D10Device::CreateGeometryShader, direct3d10.id3d10device_creategeometryshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreateGeometryShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::CreateGeometryShader


## -description


Create a geometry shader.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader. To get this pointer see <a href="https://msdn.microsoft.com/cff6f901-cb9b-44d5-a75b-9a4029a37215">Getting a Pointer to a Compiled Shader</a>.


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Size of the compiled geometry shader.


### -param ppGeometryShader [out]

Type: <b><a href="https://msdn.microsoft.com/ffe713b9-93d6-4e0a-9cf6-014ac6b8a692">ID3D10GeometryShader</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/ffe713b9-93d6-4e0a-9cf6-014ac6b8a692">ID3D10GeometryShader Interface</a>.  If this is <b>NULL</b>, all other parameters will be validated, and if all parameters pass validation this API will return S_FALSE instead of S_OK.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



Once created, the shader can be set to the device by calling <a href="https://msdn.microsoft.com/cd591f9d-dd17-48e3-b952-9f38c7572b93">ID3D10Device::GSSetShader</a>.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

