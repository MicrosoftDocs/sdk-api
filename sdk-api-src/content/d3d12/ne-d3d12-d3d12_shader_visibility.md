---
UID: NE:d3d12.D3D12_SHADER_VISIBILITY
title: D3D12_SHADER_VISIBILITY
author: windows-sdk-content
description: Specifies the shaders that can access the contents of a given root signature slot.
old-location: direct3d12\d3d12_shader_visibility.htm
tech.root: direct3d12
ms.assetid: 1D66344A-110E-4190-BC00-9F88F1A3F8FB
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_SHADER_VISIBILITY, D3D12_SHADER_VISIBILITY enumeration, D3D12_SHADER_VISIBILITY_ALL, D3D12_SHADER_VISIBILITY_DOMAIN, D3D12_SHADER_VISIBILITY_GEOMETRY, D3D12_SHADER_VISIBILITY_HULL, D3D12_SHADER_VISIBILITY_PIXEL, D3D12_SHADER_VISIBILITY_VERTEX, d3d12/D3D12_SHADER_VISIBILITY, d3d12/D3D12_SHADER_VISIBILITY_ALL, d3d12/D3D12_SHADER_VISIBILITY_DOMAIN, d3d12/D3D12_SHADER_VISIBILITY_GEOMETRY, d3d12/D3D12_SHADER_VISIBILITY_HULL, d3d12/D3D12_SHADER_VISIBILITY_PIXEL, d3d12/D3D12_SHADER_VISIBILITY_VERTEX, direct3d12.d3d12_shader_visibility
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - D3D12_SHADER_VISIBILITY
product: Windows
targetos: Windows
req.typenames: D3D12_SHADER_VISIBILITY
req.redist: 
---

# D3D12_SHADER_VISIBILITY enumeration


## -description


Specifies the shaders that can access the contents of a given root signature slot.


## -enum-fields




### -field D3D12_SHADER_VISIBILITY_ALL

Specifies that all shader stages can access whatever is bound at the root signature slot.


### -field D3D12_SHADER_VISIBILITY_VERTEX

Specifies that the vertex shader stage can access whatever is bound at the root signature slot.


### -field D3D12_SHADER_VISIBILITY_HULL

Specifies that the hull shader stage can access whatever is bound at the root signature slot.


### -field D3D12_SHADER_VISIBILITY_DOMAIN

Specifies that the domain shader stage can access whatever is bound at the root signature slot.


### -field D3D12_SHADER_VISIBILITY_GEOMETRY

Specifies that the geometry shader stage can access whatever is bound at the root signature slot.


### -field D3D12_SHADER_VISIBILITY_PIXEL

Specifies that the pixel shader stage can access whatever is bound at the root signature slot.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/CC1DFE85-7F83-4551-86C6-1AFDF746FC92">D3D12_ROOT_PARAMETER</a> structure.

The compute queue always uses <b>D3D12_SHADER_VISIBILITY_ALL</b> because it has only one active stage. The 3D queue can choose values, but if it uses <b>D3D12_SHADER_VISIBILITY_ALL</b>, all shader stages can access whatever is bound at the root signature slot.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

