---
UID: NF:d3d10.ID3D10Device.GSSetShaderResources
title: ID3D10Device::GSSetShaderResources (d3d10.h)
description: Bind an array of shader resources to the geometry shader stage.helpviewer_keywords: ["GSSetShaderResources","GSSetShaderResources method [Direct3D 10]","GSSetShaderResources method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","GSSetShaderResources method","ID3D10Device.GSSetShaderResources","ID3D10Device::GSSetShaderResources","ae1befd7-901e-0bc8-c1d4-e5f83866bff2","d3d10/ID3D10Device::GSSetShaderResources","direct3d10.id3d10device_gssetshaderresources"]
old-location: direct3d10\id3d10device_gssetshaderresources.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_gssetshaderresources.htm
ms.date: 12/05/2018
ms.keywords: GSSetShaderResources, GSSetShaderResources method [Direct3D 10], GSSetShaderResources method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GSSetShaderResources method, ID3D10Device.GSSetShaderResources, ID3D10Device::GSSetShaderResources, ae1befd7-901e-0bc8-c1d4-e5f83866bff2, d3d10/ID3D10Device::GSSetShaderResources, direct3d10.id3d10device_gssetshaderresources
f1_keywords:
- d3d10/ID3D10Device.GSSetShaderResources
dev_langs:
- c++
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D10.lib
- D3D10.dll
api_name:
- ID3D10Device.GSSetShaderResources
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Device::GSSetShaderResources


## -description


Bind an array of shader resources to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/geometry-shader-stage">geometry shader stage</a>.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin setting shader resources to.


### -param NumViews [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of shader resources to set. Up to a maximum of 128 slots are available for shader resources.


### -param ppShaderResourceViews [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView</a>*</b>

Array of <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">shader resource view</a> interfaces to set to the device.


## -remarks



If you bind a subresource as an input and an output, this API will fill the destination shader resource slot with <b>NULL</b>. The debug layer (when active) will alert you if this is true.

For information about creating shader-resource views, see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createshaderresourceview">ID3D10Device::CreateShaderResourceView</a>.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
 

 

