---
UID: NF:d3d11.ID3D11Device.CreatePixelShader
title: ID3D11Device::CreatePixelShader
author: windows-sdk-content
description: Create a pixel shader.
old-location: direct3d11\id3d11device_createpixelshader.htm
old-project: direct3d11
ms.assetid: f013a648-fd11-417b-8f87-36a4be901715
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: 60e28609-f849-5247-ceff-56bd9925d775, CreatePixelShader, CreatePixelShader method [Direct3D 11], CreatePixelShader method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreatePixelShader method, ID3D11Device.CreatePixelShader, ID3D11Device::CreatePixelShader, d3d11/ID3D11Device::CreatePixelShader, direct3d11.id3d11device_createpixelshader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CreatePixelShader
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::CreatePixelShader


## -description


Create a pixel shader.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader. 


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Size of the compiled pixel shader.


### -param pClassLinkage [in, optional]

Type: <b><a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>*</b>

A pointer to a class linkage interface (see <a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>); the value can be <b>NULL</b>.


### -param ppPixelShader [out, optional]

Type: <b><a href="https://msdn.microsoft.com/d16e00a9-02f9-413f-b9f7-31446fb0a692">ID3D11PixelShader</a>**</b>

Address of a pointer to a <a href="https://msdn.microsoft.com/d16e00a9-02f9-413f-b9f7-31446fb0a692">ID3D11PixelShader</a> interface. If this is <b>NULL</b>, all other parameters will be validated, and if all parameters pass validation this API will return S_FALSE instead of S_OK.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



After creating the pixel shader, you can set it to the device using <a href="https://msdn.microsoft.com/2ee5c946-10bd-40b0-90b2-015aff2377aa">ID3D11DeviceContext::PSSetShader</a>.




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

