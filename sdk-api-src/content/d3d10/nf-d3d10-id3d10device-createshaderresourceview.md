---
UID: NF:d3d10.ID3D10Device.CreateShaderResourceView
title: ID3D10Device::CreateShaderResourceView (d3d10.h)
description: Create a shader-resource view for accessing data in a resource.helpviewer_keywords: ["0714089a-e113-6e43-f46d-91d40fd54005","CreateShaderResourceView","CreateShaderResourceView method [Direct3D 10]","CreateShaderResourceView method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CreateShaderResourceView method","ID3D10Device.CreateShaderResourceView","ID3D10Device::CreateShaderResourceView","d3d10/ID3D10Device::CreateShaderResourceView","direct3d10.id3d10device_createshaderresourceview"]
old-location: direct3d10\id3d10device_createshaderresourceview.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createshaderresourceview.htm
ms.date: 12/05/2018
ms.keywords: 0714089a-e113-6e43-f46d-91d40fd54005, CreateShaderResourceView, CreateShaderResourceView method [Direct3D 10], CreateShaderResourceView method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateShaderResourceView method, ID3D10Device.CreateShaderResourceView, ID3D10Device::CreateShaderResourceView, d3d10/ID3D10Device::CreateShaderResourceView, direct3d10.id3d10device_createshaderresourceview
f1_keywords:
- d3d10/ID3D10Device.CreateShaderResourceView
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
- ID3D10Device.CreateShaderResourceView
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Device::CreateShaderResourceView


## -description


Create a shader-resource <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">view</a> for accessing data in a resource.


## -parameters




### -param pResource [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>*</b>

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">resource</a> that will serve as input to a shader. This resource must have been created with the <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag">D3D10_BIND_SHADER_RESOURCE</a> flag.


### -param pDesc [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_shader_resource_view_desc">D3D10_SHADER_RESOURCE_VIEW_DESC</a>*</b>

Pointer to a shader-resource-view description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_shader_resource_view_desc">D3D10_SHADER_RESOURCE_VIEW_DESC</a>). Set this parameter to <b>NULL</b> to create a view that accesses the entire resource (using the format the resource was created with).


### -param ppSRView [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView</a>**</b>

Address of a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView</a>. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -remarks



A resource is made up of one or more <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresources</a>, a view identifies which subresources to allow the pipeline to access. In addition, each resource is bound to the pipeline using a view. A shader-resource view is designed to bind any buffer or texture resource to the <a href="https://docs.microsoft.com/previous-versions/bb205146(v=vs.85)">shader stages</a> using the following API methods: <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshaderresources">VSSetShaderResources</a>, <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshaderresources">GSSetShaderResources</a> and <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshaderresources">PSSetShaderResources</a>.

Since a view is fully typed, this means that typeless resources become fully typed when bound to the pipeline.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
 

 

