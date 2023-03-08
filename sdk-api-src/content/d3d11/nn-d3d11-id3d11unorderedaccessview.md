---
UID: NN:d3d11.ID3D11UnorderedAccessView
title: ID3D11UnorderedAccessView (d3d11.h)
description: A view interface specifies the parts of a resource the pipeline can access during rendering. (ID3D11UnorderedAccessView)
helpviewer_keywords: ["0d091716-fdf1-7aff-5a05-68258dd1f745","ID3D11UnorderedAccessView","ID3D11UnorderedAccessView interface [Direct3D 11]","ID3D11UnorderedAccessView interface [Direct3D 11]","described","d3d11/ID3D11UnorderedAccessView","direct3d11.id3d11unorderedaccessview"]
old-location: direct3d11\id3d11unorderedaccessview.htm
tech.root: direct3d11
ms.assetid: 9def4a7d-f145-4073-8d7d-bf3c7ac7a060
ms.date: 12/05/2018
ms.keywords: 0d091716-fdf1-7aff-5a05-68258dd1f745, ID3D11UnorderedAccessView, ID3D11UnorderedAccessView interface [Direct3D 11], ID3D11UnorderedAccessView interface [Direct3D 11],described, d3d11/ID3D11UnorderedAccessView, direct3d11.id3d11unorderedaccessview
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
 - ID3D11UnorderedAccessView
 - d3d11/ID3D11UnorderedAccessView
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
 - ID3D11UnorderedAccessView
---

# ID3D11UnorderedAccessView interface


## -description

A view interface specifies the parts of a resource the pipeline can access during rendering.

## -inheritance

The <b>ID3D11UnorderedAccessView</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a>. <b>ID3D11UnorderedAccessView</b> also has these types of members:

## -remarks

To create a view for an unordered access resource, call  <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createunorderedaccessview">ID3D11Device::CreateUnorderedAccessView</a>.

All resources must be bound to the pipeline before they can be accessed. Call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews">ID3D11DeviceContext::CSSetUnorderedAccessViews</a> to bind an unordered access view to a compute shader; call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</a> to bind an unordered access view to a pixel shader.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-interfaces">Resource Interfaces</a>
