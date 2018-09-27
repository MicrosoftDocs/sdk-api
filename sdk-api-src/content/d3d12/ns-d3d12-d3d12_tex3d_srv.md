---
UID: NS:d3d12.D3D12_TEX3D_SRV
title: D3D12_TEX3D_SRV
author: windows-sdk-content
description: Describes the subresources from a 3D texture to use in a shader-resource view.
old-location: direct3d12\d3d12_tex3d_srv.htm
tech.root: direct3d12
ms.assetid: 21133B2B-7E12-489A-9AD6-4ACB6E6BAABC
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D12_TEX3D_SRV, D3D12_TEX3D_SRV structure, d3d12/D3D12_TEX3D_SRV, direct3d12.d3d12_tex3d_srv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12.h
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
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_TEX3D_SRV
product: Windows
targetos: Windows
req.typenames: D3D12_TEX3D_SRV
req.redist: 
---

# D3D12_TEX3D_SRV structure


## -description


Describes the subresources from a 3D texture to use in a shader-resource view.


## -struct-fields




### -field MostDetailedMip

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b> (from the original Texture3D for which <a href="https://msdn.microsoft.com/4FD7082D-2DA9-469E-BA74-6735D407D5FE">ID3D12Device::CreateShaderResourceView</a> creates a view) -1.


### -field MipLevels

The maximum number of mipmap levels for the view of the texture. See the remarks in <a href="https://msdn.microsoft.com/552DC1C1-8FFB-4BFC-8781-78B287CB70BD">D3D12_TEX1D_SRV</a>.

Set to -1 to indicate all the mipmap levels from <b>MostDetailedMip</b> on down to least detailed.


### -field ResourceMinLODClamp

A value to clamp sample LOD values to. For example, if you specify 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.


## -remarks



This structure is one member of a shader-resource-view description, <a href="https://msdn.microsoft.com/2B4B868F-3E9F-4570-B1C7-2767ED717A3B">D3D12_SHADER_RESOURCE_VIEW_DESC</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

