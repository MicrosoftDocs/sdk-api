---
UID: NF:d3d11.ID3D11DeviceContext.PSSetShader
title: ID3D11DeviceContext::PSSetShader
author: windows-sdk-content
description: Sets a pixel shader to the device.
old-location: direct3d11\id3d11devicecontext_pssetshader.htm
tech.root: direct3d11
ms.assetid: 2ee5c946-10bd-40b0-90b2-015aff2377aa
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 4cf3d515-f3f8-76b0-407a-e411a6589c75, ID3D11DeviceContext interface [Direct3D 11],PSSetShader method, ID3D11DeviceContext.PSSetShader, ID3D11DeviceContext::PSSetShader, PSSetShader, PSSetShader method [Direct3D 11], PSSetShader method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::PSSetShader, direct3d11.id3d11devicecontext_pssetshader
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.PSSetShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::PSSetShader


## -description


Sets a pixel shader to the device.


## -parameters




### -param pPixelShader [in, optional]

Type: <b><a href="https://msdn.microsoft.com/d16e00a9-02f9-413f-b9f7-31446fb0a692">ID3D11PixelShader</a>*</b>

Pointer to a pixel shader (see <a href="https://msdn.microsoft.com/d16e00a9-02f9-413f-b9f7-31446fb0a692">ID3D11PixelShader</a>). Passing in <b>NULL</b> disables the shader for this pipeline stage.
          


### -param ppClassInstances [in, optional]

Type: <b><a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>*</b>

A pointer to an array of class-instance interfaces (see <a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>). Each interface used by a shader must have a corresponding class instance or the shader will get disabled. Set ppClassInstances to <b>NULL</b> if the shader does not use any interfaces.
          


### -param NumClassInstances

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of class-instance interfaces in the array.


## -returns



This method does not return a value.




## -remarks



The method will hold a reference to the interfaces passed in.
          This differs from the device state behavior in Direct3D 10.
        

The maximum number of instances a shader can have is 256.

Set ppClassInstances to <b>NULL</b> if no interfaces are used in the shader. If it is not <b>NULL</b>, the number of class instances must match the number of interfaces used in the shader. Furthermore, each interface pointer must have a corresponding class instance or the assigned shader will be disabled.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

