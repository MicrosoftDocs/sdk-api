---
UID: NN:d3d11.ID3D11ComputeShader
title: ID3D11ComputeShader
author: windows-sdk-content
description: A compute-shader interface manages an executable program (a compute shader) that controls the compute-shader stage.
old-location: direct3d11\id3d11computeshader.htm
tech.root: direct3d11
ms.assetid: 33a43253-ada2-4085-9401-e84562b37d59
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11ComputeShader, ID3D11ComputeShader interface [Direct3D 11], ID3D11ComputeShader interface [Direct3D 11],described, d3d11/ID3D11ComputeShader, dde07f60-78d4-2f2f-10da-d2a2973a909c, direct3d11.id3d11computeshader
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11ComputeShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ComputeShader interface


## -description


A compute-shader interface manages an executable program (a compute shader) that controls the compute-shader stage.


## -remarks



The compute-shader interface has no methods; use HLSL to implement your shader functionality. All shaders are implemented from a common set of features referred to as the common-shader core..

To create a compute-shader interface, call <a href="https://msdn.microsoft.com/4ee0f4f5-48dc-4d5a-b159-c1b7f72e5367">ID3D11Device::CreateComputeShader</a>. Before using a compute shader you must bind it to the device by calling <a href="https://msdn.microsoft.com/97be7622-609f-4576-911a-93aa7f1b6b8c">ID3D11DeviceContext::CSSetShader</a>.

This interface is defined in D3D11.h.




## -see-also




<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

