---
UID: NF:d3d11.ID3D11DeviceContext.HSSetShader
title: ID3D11DeviceContext::HSSetShader method
author: windows-driver-content
description: Set a hull shader to the device.
old-location: direct3d11\id3d11devicecontext_hssetshader.htm
old-project: direct3d11
ms.assetid: e540f88f-fbf8-4135-b1ee-873ec18bc2c8
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 12c23e83-63d7-9b87-4fe7-75e515f02660, HSSetShader method [Direct3D 11], HSSetShader method [Direct3D 11], ID3D11DeviceContext interface, HSSetShader,ID3D11DeviceContext.HSSetShader, ID3D11DeviceContext, ID3D11DeviceContext interface [Direct3D 11], HSSetShader method, ID3D11DeviceContext::HSSetShader, d3d11/ID3D11DeviceContext::HSSetShader, direct3d11.id3d11devicecontext_hssetshader
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11DeviceContext.HSSetShader
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::HSSetShader method


## -description


Set a hull shader to the device.


## -parameters




### -param pHullShader [in, optional]

Type: <b><a href="https://msdn.microsoft.com/3459f533-e2ac-4b0e-bfdd-d9dae704f418">ID3D11HullShader</a>*</b>

Pointer to a hull shader (see <a href="https://msdn.microsoft.com/3459f533-e2ac-4b0e-bfdd-d9dae704f418">ID3D11HullShader</a>). Passing in <b>NULL</b> disables the shader for this pipeline stage.


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
 

 

