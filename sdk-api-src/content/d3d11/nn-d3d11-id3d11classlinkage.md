---
UID: NN:d3d11.ID3D11ClassLinkage
title: ID3D11ClassLinkage (d3d11.h)
description: This interface encapsulates an HLSL dynamic linkage.
helpviewer_keywords: ["6153eaad-32d7-c087-4631-725183e63035","ID3D11ClassLinkage","ID3D11ClassLinkage interface [Direct3D 11]","ID3D11ClassLinkage interface [Direct3D 11]","described","d3d11/ID3D11ClassLinkage","direct3d11.id3d11classlinkage"]
old-location: direct3d11\id3d11classlinkage.htm
tech.root: direct3d11
ms.assetid: eac03911-d881-4304-9598-912321ac0b0c
ms.date: 12/05/2018
ms.keywords: 6153eaad-32d7-c087-4631-725183e63035, ID3D11ClassLinkage, ID3D11ClassLinkage interface [Direct3D 11], ID3D11ClassLinkage interface [Direct3D 11],described, d3d11/ID3D11ClassLinkage, direct3d11.id3d11classlinkage
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
 - ID3D11ClassLinkage
 - d3d11/ID3D11ClassLinkage
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
 - ID3D11ClassLinkage
---

# ID3D11ClassLinkage interface


## -description

This interface encapsulates an HLSL dynamic linkage.

## -inheritance

The <b>ID3D11ClassLinkage</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11ClassLinkage</b> also has these types of members:

## -remarks

A class linkage object can hold up to 64K gotten instances. A gotten instance is a handle that references a variable name in any shader that is created with that linkage object. When you create a shader with a class linkage object, the runtime gathers these instances and stores them in the class linkage object. For more information about how a class linkage object is used, see <a href="/windows/desktop/direct3dhlsl/storing-variables-and-types-for-shaders-to-share">Storing Variables and Types for Shaders to Share</a>.

An <b>ID3D11ClassLinkage</b> object is created using the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createclasslinkage">ID3D11Device::CreateClassLinkage</a> method.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
