---
UID: NF:d3d11.ID3D11DeviceContext.CSGetShader
title: ID3D11DeviceContext::CSGetShader
author: windows-sdk-content
description: Get the compute shader currently set on the device.
old-location: direct3d11\id3d11devicecontext_csgetshader.htm
old-project: direct3d11
ms.assetid: ddd09ca8-ab1f-4d1d-a182-44e48bac93c5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CSGetShader, CSGetShader method [Direct3D 11], CSGetShader method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CSGetShader method, ID3D11DeviceContext.CSGetShader, ID3D11DeviceContext::CSGetShader, d3d11/ID3D11DeviceContext::CSGetShader, d55a8dcd-a09c-0388-1870-f4bcb519d6b1, direct3d11.id3d11devicecontext_csgetshader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
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
 - ID3D11DeviceContext.CSGetShader
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::CSGetShader


## -description


Get the compute shader currently set on the device.


## -parameters




### -param ppComputeShader [out]

Type: <b><a href="https://msdn.microsoft.com/33a43253-ada2-4085-9401-e84562b37d59">ID3D11ComputeShader</a>**</b>

Address of a pointer to a Compute shader (see <a href="https://msdn.microsoft.com/33a43253-ada2-4085-9401-e84562b37d59">ID3D11ComputeShader</a>) to be returned by the method.


### -param ppClassInstances [out, optional]

Type: <b><a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>**</b>

Pointer to an array of class instance interfaces (see <a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>).


### -param pNumClassInstances [in, out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

The number of class-instance elements in the array.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

