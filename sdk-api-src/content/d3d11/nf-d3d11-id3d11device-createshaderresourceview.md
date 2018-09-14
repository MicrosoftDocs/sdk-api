---
UID: NF:d3d11.ID3D11Device.CreateShaderResourceView
title: ID3D11Device::CreateShaderResourceView
author: windows-sdk-content
description: Create a shader-resource view for accessing data in a resource.
old-location: direct3d11\id3d11device_createshaderresourceview.htm
tech.root: direct3d11
ms.assetid: a8e3cda3-76f9-48c3-9e0c-e530f95fe8b8
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 6f2fff53-b73d-3404-2005-37078d5f283b, CreateShaderResourceView, CreateShaderResourceView method [Direct3D 11], CreateShaderResourceView method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateShaderResourceView method, ID3D11Device.CreateShaderResourceView, ID3D11Device::CreateShaderResourceView, d3d11/ID3D11Device::CreateShaderResourceView, direct3d11.id3d11device_createshaderresourceview
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CreateShaderResourceView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device::CreateShaderResourceView


## -description


Create a shader-resource view for accessing data in a resource.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

Pointer to the resource that will serve as input to a shader. This resource must have been created with the <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_SHADER_RESOURCE
            </a> flag.
          


### -param pDesc [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/7ce09172-8a01-4718-b0ef-0ae118a9be16">D3D11_SHADER_RESOURCE_VIEW_DESC</a>*</b>

Pointer to a shader-resource view description (see <a href="https://msdn.microsoft.com/7ce09172-8a01-4718-b0ef-0ae118a9be16">D3D11_SHADER_RESOURCE_VIEW_DESC</a>). Set this parameter to <b>NULL</b> to create a
            view that accesses the entire resource (using the format the resource was created with).
          


### -param ppSRView [out, optional]

Type: <b><a href="https://msdn.microsoft.com/289555d8-2a6e-454f-86bc-48fb2c8ea345">ID3D11ShaderResourceView</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/289555d8-2a6e-454f-86bc-48fb2c8ea345">ID3D11ShaderResourceView</a>. Set this parameter to <b>NULL</b> to validate the
            other input parameters (the method will return <b>S_FALSE</b> if the other input parameters pass validation).
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -remarks



A resource is made up of one or more subresources; a view identifies which subresources to allow the pipeline to access. In addition, each resource is
          bound to the pipeline using a view. A shader-resource view is designed to bind any buffer or texture resource to the shader stages using the following
          API methods: <a href="https://msdn.microsoft.com/f5dbd212-6896-41b1-b61b-f1c1a690a195">ID3D11DeviceContext::VSSetShaderResources</a>, <a href="https://msdn.microsoft.com/f08af865-ec0a-4fc7-af59-004b6956be00">ID3D11DeviceContext::GSSetShaderResources</a>and <a href="https://msdn.microsoft.com/acccbde4-68d0-4c76-bf77-643884af1bbe">ID3D11DeviceContext::PSSetShaderResources</a>.
        

Because a view is fully typed, this means that typeless resources become fully typed when bound to the pipeline.

<div class="alert"><b>Note</b>  To successfully create a shader-resource view from a typeless buffer (for example, <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R32G32B32A32_TYPELESS</a>), you must set the <a href="d3d11_resource_misc_flag.htm">D3D11_RESOURCE_MISC_BUFFER_ALLOW_RAW_VIEWS</a> flag when you create the buffer.
        </div>
<div> </div>
The Direct3D 11.1 runtime, which is available starting with Windows 8, allows you to use <b>CreateShaderResourceView</b> for the following new purpose.
        

You can create shader-resource views of video resources so that Direct3D shaders can process those shader-resource views. These video resources are either <a href="https://msdn.microsoft.com/e4f9cfd8-65e6-4375-8f87-736bca32cad4">Texture2D</a> or <a href="https://msdn.microsoft.com/78ab2feb-4d67-4f6f-bffe-48d55183ce28">Texture2DArray</a>. The value in the <b>ViewDimension</b> member of the <a href="https://msdn.microsoft.com/7ce09172-8a01-4718-b0ef-0ae118a9be16">D3D11_SHADER_RESOURCE_VIEW_DESC</a> structure for a created shader-resource view must match the type of video resource, D3D11_SRV_DIMENSION_TEXTURE2D          for Texture2D and D3D11_SRV_DIMENSION_TEXTURE2DARRAY for Texture2DArray. Additionally, the format of the underlying video resource restricts the formats that the view can use. The video resource format values on the <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> reference page specify the format values that views are restricted to.
        

The runtime read+write conflict prevention logic (which stops a resource from being bound as an SRV and RTV or UAV at the same time) treats views of different parts of the same video surface as conflicting for simplicity.  Therefore, the runtime does not allow an application to read from luma while the application simultaneously renders to chroma in the same surface even though the hardware might allow these simultaneous operations.

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

