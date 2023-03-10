---
UID: NF:d3d11.ID3D11Device.CreateUnorderedAccessView
title: ID3D11Device::CreateUnorderedAccessView (d3d11.h)
description: Creates a view for accessing an unordered access resource. (ID3D11Device.CreateUnorderedAccessView)
helpviewer_keywords: ["CreateUnorderedAccessView","CreateUnorderedAccessView method [Direct3D 11]","CreateUnorderedAccessView method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateUnorderedAccessView method","ID3D11Device.CreateUnorderedAccessView","ID3D11Device::CreateUnorderedAccessView","d3d11/ID3D11Device::CreateUnorderedAccessView","direct3d11.id3d11device_createunorderedaccessview","e40c2139-4401-eb51-d806-6b5f91c06ee6"]
old-location: direct3d11\id3d11device_createunorderedaccessview.htm
tech.root: direct3d11
ms.assetid: 85b85114-4e3f-407e-879c-ef4c120cb3c1
ms.date: 12/05/2018
ms.keywords: CreateUnorderedAccessView, CreateUnorderedAccessView method [Direct3D 11], CreateUnorderedAccessView method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateUnorderedAccessView method, ID3D11Device.CreateUnorderedAccessView, ID3D11Device::CreateUnorderedAccessView, d3d11/ID3D11Device::CreateUnorderedAccessView, direct3d11.id3d11device_createunorderedaccessview, e40c2139-4401-eb51-d806-6b5f91c06ee6
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device::CreateUnorderedAccessView
 - d3d11/ID3D11Device::CreateUnorderedAccessView
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
 - ID3D11Device.CreateUnorderedAccessView
---

# ID3D11Device::CreateUnorderedAccessView


## -description

Creates a view for accessing an <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources">unordered access</a> resource.

## -parameters

### -param pResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> that represents a resources that will serve as an input to a shader.

### -param pDesc [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_unordered_access_view_desc">D3D11_UNORDERED_ACCESS_VIEW_DESC</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_unordered_access_view_desc">D3D11_UNORDERED_ACCESS_VIEW_DESC</a> that represents a shader-resource view description. Set this parameter to <b>NULL</b> to create a view that accesses the entire resource (using the format the resource was created with).

### -param ppUAView [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a> that represents an unordered-access view. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

The Direct3D 11.1 runtime, which is available starting with Windows 8, allows you to use <b>CreateUnorderedAccessView</b> for the following new purpose. 

You can create unordered-access views of video resources so that Direct3D shaders can process those unordered-access views. These video resources are either <a href="/windows/desktop/direct3dhlsl/sm5-object-texture2d">Texture2D</a> or <a href="/windows/desktop/direct3dhlsl/sm5-object-texture2darray">Texture2DArray</a>. The value in the <b>ViewDimension</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_unordered_access_view_desc">D3D11_UNORDERED_ACCESS_VIEW_DESC</a> structure for a created unordered-access view must match the type of video resource, D3D11_UAV_DIMENSION_TEXTURE2D          for Texture2D and D3D11_UAV_DIMENSION_TEXTURE2DARRAY for Texture2DArray. Additionally, the format of the underlying video resource restricts the formats that the view can use. The video resource format values on the <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> reference page specify the format values that views are restricted to.

The runtime read+write conflict prevention logic (which stops a resource from being bound as an SRV and RTV or UAV at the same time) treats views of different parts of the same video surface as conflicting for simplicity.  Therefore, the runtime does not allow an application to read from luma while the application simultaneously renders to chroma in the same surface even though the hardware might allow these simultaneous operations.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
