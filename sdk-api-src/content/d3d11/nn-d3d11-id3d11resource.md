---
UID: NN:d3d11.ID3D11Resource
title: ID3D11Resource (d3d11.h)
description: A resource interface provides common actions on all resources. (ID3D11Resource)
helpviewer_keywords: ["ID3D11Resource","ID3D11Resource interface [Direct3D 11]","ID3D11Resource interface [Direct3D 11]","described","d3d11/ID3D11Resource","d8e977b3-ff67-b931-bf00-8a95c24e06b7","direct3d11.id3d11resource"]
old-location: direct3d11\id3d11resource.htm
tech.root: direct3d11
ms.assetid: 3823ec00-cb3c-43ce-9f1a-be4e1e99d587
ms.date: 12/05/2018
ms.keywords: ID3D11Resource, ID3D11Resource interface [Direct3D 11], ID3D11Resource interface [Direct3D 11],described, d3d11/ID3D11Resource, d8e977b3-ff67-b931-bf00-8a95c24e06b7, direct3d11.id3d11resource
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
 - ID3D11Resource
 - d3d11/ID3D11Resource
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
 - ID3D11Resource
---

# ID3D11Resource interface


## -description

A resource interface provides common actions on all resources.

## -inheritance

The <b>ID3D11Resource</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11Resource</b> also has these types of members:

## -remarks

You don't directly create a resource interface; instead, you create buffers and textures that inherit from a resource interface. For more info,  see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to">How to: Create a Vertex Buffer</a>, <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to">How to: Create an Index Buffer</a>, <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to">How to: Create a Constant Buffer</a>, and <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create">How to: Create a Texture</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-interfaces">Resource Interfaces</a>
