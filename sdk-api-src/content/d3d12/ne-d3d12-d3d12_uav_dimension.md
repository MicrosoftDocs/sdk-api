---
UID: NE:d3d12.D3D12_UAV_DIMENSION
title: D3D12_UAV_DIMENSION
author: windows-driver-content
description: Identifies unordered-access view options.
old-location: direct3d12\d3d12_uav_dimension.htm
old-project: direct3d12
ms.assetid: 2D4DA7D4-8AC6-4507-BCC2-FB5C5431BB73
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: D3D12_UAV_DIMENSION, D3D12_UAV_DIMENSION enumeration, D3D12_UAV_DIMENSION_BUFFER, D3D12_UAV_DIMENSION_TEXTURE1D, D3D12_UAV_DIMENSION_TEXTURE1DARRAY, D3D12_UAV_DIMENSION_TEXTURE2D, D3D12_UAV_DIMENSION_TEXTURE2DARRAY, D3D12_UAV_DIMENSION_TEXTURE3D, D3D12_UAV_DIMENSION_UNKNOWN, d3d12/D3D12_UAV_DIMENSION, d3d12/D3D12_UAV_DIMENSION_BUFFER, d3d12/D3D12_UAV_DIMENSION_TEXTURE1D, d3d12/D3D12_UAV_DIMENSION_TEXTURE1DARRAY, d3d12/D3D12_UAV_DIMENSION_TEXTURE2D, d3d12/D3D12_UAV_DIMENSION_TEXTURE2DARRAY, d3d12/D3D12_UAV_DIMENSION_TEXTURE3D, d3d12/D3D12_UAV_DIMENSION_UNKNOWN, direct3d12.d3d12_uav_dimension
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D12_UAV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D12.h
api_name:
-	D3D12_UAV_DIMENSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_UAV_DIMENSION enumeration


## -description


Identifies unordered-access view options.


## -enum-fields




### -field D3D12_UAV_DIMENSION_UNKNOWN

The view type is unknown.


### -field D3D12_UAV_DIMENSION_BUFFER

View the resource as a buffer.


### -field D3D12_UAV_DIMENSION_TEXTURE1D

View the resource as a 1D texture.


### -field D3D12_UAV_DIMENSION_TEXTURE1DARRAY

View the resource as a 1D texture array.


### -field D3D12_UAV_DIMENSION_TEXTURE2D

View the resource as a 2D texture.


### -field D3D12_UAV_DIMENSION_TEXTURE2DARRAY

View the resource as a 2D texture array.


### -field D3D12_UAV_DIMENSION_TEXTURE3D

View the resource as a 3D texture array.


## -remarks




          Specify one of the values in this enumeration in the <b>ViewDimension</b> member of a <a href="https://msdn.microsoft.com/0C3A31FE-625D-4CB3-87FD-D2C33D008DD4">D3D12_UNORDERED_ACCESS_VIEW_DESC</a> structure.
        




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

