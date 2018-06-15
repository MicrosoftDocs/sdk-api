---
UID: NF:d3d10.ID3D10Device.CreateDepthStencilView
title: ID3D10Device::CreateDepthStencilView
author: windows-sdk-content
description: Create a depth-stencil view for accessing resource data.
old-location: direct3d10\id3d10device_createdepthstencilview.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createdepthstencilview.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CreateDepthStencilView, CreateDepthStencilView method [Direct3D 10], CreateDepthStencilView method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateDepthStencilView method, ID3D10Device.CreateDepthStencilView, ID3D10Device::CreateDepthStencilView, d3d10/ID3D10Device::CreateDepthStencilView, direct3d10.id3d10device_createdepthstencilview, f7b0585b-710f-b4d1-e65f-c30b57116c09
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreateDepthStencilView
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::CreateDepthStencilView


## -description


Create a depth-stencil <a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">view</a> for accessing resource data.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">resource</a> that will serve as the depth-stencil surface. This resource must have been created with the <a href="https://msdn.microsoft.com/3bbefc3b-ad05-499b-bbec-f370bf08a7f4">D3D10_BIND_DEPTH_STENCIL</a> flag.


### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/7e427a75-99d7-4a18-afee-077bee01683c">D3D10_DEPTH_STENCIL_VIEW_DESC</a>*</b>

Pointer to a depth-stencil-view description (see <a href="https://msdn.microsoft.com/7e427a75-99d7-4a18-afee-077bee01683c">D3D10_DEPTH_STENCIL_VIEW_DESC</a>). Set this parameter to <b>NULL</b> to create a view that accesses mipmap level 0 of the entire resource (using the format the resource was created with).


### -param ppDepthStencilView [out]

Type: <b><a href="https://msdn.microsoft.com/b88f3b61-4549-4ef7-9dda-0c2ed247d2f1">ID3D10DepthStencilView</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/b88f3b61-4549-4ef7-9dda-0c2ed247d2f1">ID3D10DepthStencilView</a>. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



A depth-stencil view can be bound to the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a> by calling <a href="https://msdn.microsoft.com/68c20b1a-921a-4513-811b-f3b6999518f8">ID3D10Device::OMSetRenderTargets</a>.

For more background information, see the <a href="https://msdn.microsoft.com/e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f">programming guide page</a> about depth stencils.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

