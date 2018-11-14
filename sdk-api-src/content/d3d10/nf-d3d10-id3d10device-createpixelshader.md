---
UID: NF:d3d10.ID3D10Device.CreatePixelShader
title: ID3D10Device::CreatePixelShader
author: windows-sdk-content
description: Create a pixel shader.
old-location: direct3d10\id3d10device_createpixelshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createpixelshader.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreatePixelShader, CreatePixelShader method [Direct3D 10], CreatePixelShader method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreatePixelShader method, ID3D10Device.CreatePixelShader, ID3D10Device::CreatePixelShader, d3d10/ID3D10Device::CreatePixelShader, direct3d10.id3d10device_createpixelshader, eaddd998-99a2-ab8d-51dd-98d72c93e291
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
 - ID3D10Device.CreatePixelShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10.h
: 
- ID3D10Device.CreatePixelShader
: 
---

# ID3D10Device::CreatePixelShader


## -description


Create a pixel shader.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader. To get this pointer see <a href="https://msdn.microsoft.com/cff6f901-cb9b-44d5-a75b-9a4029a37215">Getting a Pointer to a Compiled Shader</a>.


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Size of the compiled pixel shader.


### -param ppPixelShader [out]

Type: <b><a href="https://msdn.microsoft.com/c2b255ca-cffb-4e24-9395-a4cb727bf421">ID3D10PixelShader</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/c2b255ca-cffb-4e24-9395-a4cb727bf421">ID3D10PixelShader Interface</a>. If this is <b>NULL</b>, all other parameters will be validated, and if all parameters pass validation this API will return S_FALSE instead of S_OK.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



After creating the pixel shader, you can set it to the device using <a href="https://msdn.microsoft.com/8e7cf7fb-e2c0-4524-a909-5592decd9a66">ID3D10Device::PSSetShader</a>.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

