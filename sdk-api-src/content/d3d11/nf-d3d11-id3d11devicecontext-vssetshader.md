---
UID: NF:d3d11.ID3D11DeviceContext.VSSetShader
title: ID3D11DeviceContext::VSSetShader
author: windows-sdk-content
description: Set a vertex shader to the device.
old-location: direct3d11\id3d11devicecontext_vssetshader.htm
tech.root: direct3d11
ms.assetid: d6207779-7477-4e74-beb8-065949abce06
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 2642b72a-9d7a-0eff-a9a4-df4e0b8eca75, ID3D11DeviceContext interface [Direct3D 11],VSSetShader method, ID3D11DeviceContext.VSSetShader, ID3D11DeviceContext::VSSetShader, VSSetShader, VSSetShader method [Direct3D 11], VSSetShader method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::VSSetShader, direct3d11.id3d11devicecontext_vssetshader
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
 - ID3D11DeviceContext.VSSetShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::VSSetShader


## -description


Set a vertex shader to the device.


## -parameters




### -param pVertexShader [in, optional]

Type: <b><a href="https://msdn.microsoft.com/8300ec12-ecf5-49c2-9313-b542a7d971f3">ID3D11VertexShader</a>*</b>

Pointer to a vertex shader (see <a href="https://msdn.microsoft.com/8300ec12-ecf5-49c2-9313-b542a7d971f3">ID3D11VertexShader</a>). Passing in <b>NULL</b> disables the shader for this pipeline stage.


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




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

