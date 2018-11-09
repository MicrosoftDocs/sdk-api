---
UID: NF:d3d10_1.ID3D10Device1.CreateShaderResourceView1
title: ID3D10Device1::CreateShaderResourceView1
author: windows-sdk-content
description: Create a shader-resource view for accessing data in a resource.
old-location: direct3d10\id3d10device1_createshaderresourceview1.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device1_createshaderresourceview1.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 03e028ae-86fb-9c0c-3e9c-3a0471355fab, CreateShaderResourceView1, CreateShaderResourceView1 method [Direct3D 10], CreateShaderResourceView1 method [Direct3D 10],ID3D10Device1 interface, ID3D10Device1 interface [Direct3D 10],CreateShaderResourceView1 method, ID3D10Device1.CreateShaderResourceView1, ID3D10Device1::CreateShaderResourceView1, d3d10_1/ID3D10Device1::CreateShaderResourceView1, direct3d10.id3d10device1_createshaderresourceview1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10_1.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10_1.h
api_name:
 - ID3D10Device1.CreateShaderResourceView1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device1::CreateShaderResourceView1


## -description


Create a shader-resource <a href="https://msdn.microsoft.com/ccfe6273-0dcf-4b42-9d74-665a0b4cd14a">view</a> for accessing data in a resource.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">resource</a> that will serve as input to a shader. This resource must have been created with the <a href="https://msdn.microsoft.com/3bbefc3b-ad05-499b-bbec-f370bf08a7f4">D3D10_BIND_SHADER_RESOURCE</a> flag.


### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/788a696d-5e39-4f7b-a7dd-860671a6d2b8">D3D10_SHADER_RESOURCE_VIEW_DESC1</a>*</b>

Pointer to a shader-resource-view description (see <a href="https://msdn.microsoft.com/788a696d-5e39-4f7b-a7dd-860671a6d2b8">D3D10_SHADER_RESOURCE_VIEW_DESC1</a>). Set this parameter to <b>NULL</b> to create a view that accesses the entire resource (using the format the resource was created with).


### -param ppSRView [out]

Type: <b><a href="https://msdn.microsoft.com/601e8261-11d5-4c2a-a0ef-f498327feb13">ID3D10ShaderResourceView1</a>**</b>

Address of a pointer to a shader-resource view (see <a href="https://msdn.microsoft.com/601e8261-11d5-4c2a-a0ef-f498327feb13">ID3D10ShaderResourceView1 Interface</a>). Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



A resource is made up of one or more <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresources</a>, a view identifies which subresources to allow the pipeline to access. In addition, each resource is bound to the pipeline using a view. A shader-resource view is designed to bind any buffer or texture resource to the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">shader stages</a> using the following API methods: <a href="https://msdn.microsoft.com/8481e388-3cfe-43e3-b58e-fea989d942ba">VSSetShaderResources</a>, <a href="https://msdn.microsoft.com/8e012e31-b161-4564-9acf-243d99366092">GSSetShaderResources</a> and <a href="https://msdn.microsoft.com/88b1515b-f070-4725-a844-30575a1800d4">PSSetShaderResources</a>.

Since a view is fully typed, this means that typeless resources become fully typed when bound to the pipeline.

This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/511f710d-f35e-46bf-93e0-47b6ceb5c84d">ID3D10Device1 Interface</a>
 

 

