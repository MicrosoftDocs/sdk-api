---
UID: NF:d3d10.ID3D10Device.PSSetShaderResources
title: ID3D10Device::PSSetShaderResources
author: windows-sdk-content
description: Bind an array of shader resources to the pixel shader stage.
old-location: direct3d10\id3d10device_pssetshaderresources.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_pssetshaderresources.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 5c6524cb-030c-fa99-f855-ac20599cb810, ID3D10Device interface [Direct3D 10],PSSetShaderResources method, ID3D10Device.PSSetShaderResources, ID3D10Device::PSSetShaderResources, PSSetShaderResources, PSSetShaderResources method [Direct3D 10], PSSetShaderResources method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::PSSetShaderResources, direct3d10.id3d10device_pssetshaderresources
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
 - ID3D10Device.PSSetShaderResources
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::PSSetShaderResources


## -description


Bind an array of shader resources to the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">pixel shader stage</a>.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into the device's zero-based array to begin setting shader resources to.


### -param NumViews [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of shader resources to set. Up to a maximum of 128 slots are available for shader resources.


### -param ppShaderResourceViews [in]

Type: <b><a href="https://msdn.microsoft.com/303076f3-6057-4f7c-9aa8-a6dd72235ecc">ID3D10ShaderResourceView</a>*</b>

Array of <a href="https://msdn.microsoft.com/303076f3-6057-4f7c-9aa8-a6dd72235ecc">shader resource view</a> interfaces to set to the device.


## -returns



Returns nothing.




## -remarks



If you bind a subresource as an input and an output, this API will fill the destination shader resource slot with <b>NULL</b>. The debug layer (when active) will alert you if this is true.

For information about creating shader-resource views, see <a href="https://msdn.microsoft.com/32e5d4d0-6686-4bcc-8ddb-fe519544051b">ID3D10Device::CreateShaderResourceView</a>.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

