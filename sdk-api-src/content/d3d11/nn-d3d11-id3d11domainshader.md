---
UID: NN:d3d11.ID3D11DomainShader
title: ID3D11DomainShader (d3d11.h)
description: A domain-shader interface manages an executable program (a domain shader) that controls the domain-shader stage.
helpviewer_keywords: ["ID3D11DomainShader","ID3D11DomainShader interface [Direct3D 11]","ID3D11DomainShader interface [Direct3D 11]","described","b1ab0261-4310-836c-a463-56ac752ba47f","d3d11/ID3D11DomainShader","direct3d11.id3d11domainshader"]
old-location: direct3d11\id3d11domainshader.htm
tech.root: direct3d11
ms.assetid: cd01c872-4df5-4741-90c5-211d3e393f89
ms.date: 12/05/2018
ms.keywords: ID3D11DomainShader, ID3D11DomainShader interface [Direct3D 11], ID3D11DomainShader interface [Direct3D 11],described, b1ab0261-4310-836c-a463-56ac752ba47f, d3d11/ID3D11DomainShader, direct3d11.id3d11domainshader
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DomainShader
 - d3d11/ID3D11DomainShader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DomainShader
---

# ID3D11DomainShader interface


## -description

A domain-shader interface manages an executable program (a domain shader) that controls the domain-shader stage.

## -remarks

The domain-shader interface has no methods; use HLSL to implement your shader functionality. All shaders are implemented from a common set of features referred to as the common-shader core..

To create a domain-shader interface, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createdomainshader">ID3D11Device::CreateDomainShader</a>. Before using a domain shader you must bind it to the device by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dssetshader">ID3D11DeviceContext::DSSetShader</a>.

This interface is defined in D3D11.h.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>