---
UID: NE:d3d10.D3D10_RESOURCE_DIMENSION
title: D3D10_RESOURCE_DIMENSION
author: windows-driver-content
description: Identifies the type of resource being used.
old-location: direct3d10\d3d10_resource_dimension.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_resource_dimension.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 63b970df-266a-f05f-9db6-cec5c9ae14a6, D3D10_RESOURCE_DIMENSION, D3D10_RESOURCE_DIMENSION enumeration [Direct3D 10], D3D10_RESOURCE_DIMENSION_BUFFER, D3D10_RESOURCE_DIMENSION_TEXTURE1D, D3D10_RESOURCE_DIMENSION_TEXTURE2D, D3D10_RESOURCE_DIMENSION_TEXTURE3D, D3D10_RESOURCE_DIMENSION_UNKNOWN, d3d10/D3D10_RESOURCE_DIMENSION, d3d10/D3D10_RESOURCE_DIMENSION_BUFFER, d3d10/D3D10_RESOURCE_DIMENSION_TEXTURE1D, d3d10/D3D10_RESOURCE_DIMENSION_TEXTURE2D, d3d10/D3D10_RESOURCE_DIMENSION_TEXTURE3D, d3d10/D3D10_RESOURCE_DIMENSION_UNKNOWN, direct3d10.d3d10_resource_dimension
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: D3D10_RESOURCE_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D10.h
api_name:
-	D3D10_RESOURCE_DIMENSION
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D3D10_RESOURCE_DIMENSION enumeration


## -description


Identifies the type of <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">resource</a> being used.


## -enum-fields




### -field D3D10_RESOURCE_DIMENSION_UNKNOWN

Resource is of unknown type.


### -field D3D10_RESOURCE_DIMENSION_BUFFER

Resource is a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">buffer</a>.


### -field D3D10_RESOURCE_DIMENSION_TEXTURE1D

Resource is a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">1D texture</a>.


### -field D3D10_RESOURCE_DIMENSION_TEXTURE2D

Resource is a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">2D texture</a>.


### -field D3D10_RESOURCE_DIMENSION_TEXTURE3D

Resource is a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">3D texture</a>.


## -remarks



This enumeration is used in <a href="https://msdn.microsoft.com/78e91654-e3e7-4565-99be-8ccf480b954b">ID3D10Resource::GetType</a>, and <a href="https://msdn.microsoft.com/40d89166-cc11-490d-867c-ae5db23a0784">D3DX10_IMAGE_INFO</a>.




## -see-also




<a href="https://msdn.microsoft.com/c986b22c-2960-4571-98bc-028c9f41ec65">Resource Enumerations</a>
 

 

