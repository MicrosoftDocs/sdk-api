---
UID: NN:d3d11.ID3D11DomainShader
title: ID3D11DomainShader
author: windows-driver-content
description: A domain-shader interface manages an executable program (a domain shader) that controls the domain-shader stage.
old-location: direct3d11\id3d11domainshader.htm
old-project: direct3d11
ms.assetid: cd01c872-4df5-4741-90c5-211d3e393f89
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ID3D11DomainShader, ID3D11DomainShader interface [Direct3D 11], ID3D11DomainShader interface [Direct3D 11], described, b1ab0261-4310-836c-a463-56ac752ba47f, d3d11/ID3D11DomainShader, direct3d11.id3d11domainshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
-	ID3D11DomainShader
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DomainShader interface


## -description


A domain-shader interface manages an executable program (a domain shader) that controls the domain-shader stage.


## -remarks



The domain-shader interface has no methods; use HLSL to implement your shader functionality. All shaders are implemented from a common set of features referred to as the common-shader core..

To create a domain-shader interface, call <a href="https://msdn.microsoft.com/414525a8-55ad-4d37-a302-5c30909588f1">ID3D11Device::CreateDomainShader</a>. Before using a domain shader you must bind it to the device by calling <a href="https://msdn.microsoft.com/5ee4a072-3b4a-44e6-ae70-19e0888905a2">ID3D11DeviceContext::DSSetShader</a>.

This interface is defined in D3D11.h.




## -see-also




<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

