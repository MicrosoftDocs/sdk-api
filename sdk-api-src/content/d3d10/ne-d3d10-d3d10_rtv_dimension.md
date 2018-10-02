---
UID: NE:d3d10.D3D10_RTV_DIMENSION
title: D3D10_RTV_DIMENSION
author: windows-sdk-content
description: Specifies how to access a resource used in a render-target view.
old-location: direct3d10\d3d10_rtv_dimension.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_rtv_dimension.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D10_RTV_DIMENSION, D3D10_RTV_DIMENSION enumeration [Direct3D 10], D3D10_RTV_DIMENSION_BUFFER, D3D10_RTV_DIMENSION_TEXTURE1D, D3D10_RTV_DIMENSION_TEXTURE1DARRAY, D3D10_RTV_DIMENSION_TEXTURE2D, D3D10_RTV_DIMENSION_TEXTURE2DARRAY, D3D10_RTV_DIMENSION_TEXTURE2DMS, D3D10_RTV_DIMENSION_TEXTURE2DMSARRAY, D3D10_RTV_DIMENSION_TEXTURE3D, D3D10_RTV_DIMENSION_UNKNOWN, d3d10/D3D10_RTV_DIMENSION, d3d10/D3D10_RTV_DIMENSION_BUFFER, d3d10/D3D10_RTV_DIMENSION_TEXTURE1D, d3d10/D3D10_RTV_DIMENSION_TEXTURE1DARRAY, d3d10/D3D10_RTV_DIMENSION_TEXTURE2D, d3d10/D3D10_RTV_DIMENSION_TEXTURE2DARRAY, d3d10/D3D10_RTV_DIMENSION_TEXTURE2DMS, d3d10/D3D10_RTV_DIMENSION_TEXTURE2DMSARRAY, d3d10/D3D10_RTV_DIMENSION_TEXTURE3D, d3d10/D3D10_RTV_DIMENSION_UNKNOWN, direct3d10.d3d10_rtv_dimension, ee7da179-55ef-38ba-f14d-1b95f3eb9520
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_RTV_DIMENSION
product: Windows
targetos: Windows
req.typenames: D3D10_RTV_DIMENSION
req.redist: 
---

# D3D10_RTV_DIMENSION enumeration


## -description


Specifies how to access a resource used in a render-target <a href="https://msdn.microsoft.com/ccfe6273-0dcf-4b42-9d74-665a0b4cd14a">view</a>.


## -enum-fields




### -field D3D10_RTV_DIMENSION_UNKNOWN

The resource will be accessed according to its type as determined from the actual instance this enumeration is paired with when the render-target view is created.


### -field D3D10_RTV_DIMENSION_BUFFER

The resource will be accessed as a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">buffer</a>.


### -field D3D10_RTV_DIMENSION_TEXTURE1D

The resource will be accessed as a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">1D texture</a>.


### -field D3D10_RTV_DIMENSION_TEXTURE1DARRAY

The resource will be accessed as an array of 1D textures.


### -field D3D10_RTV_DIMENSION_TEXTURE2D

The resource will be accessed as a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">2D texture</a>.


### -field D3D10_RTV_DIMENSION_TEXTURE2DARRAY

The resource will be accessed as an array of 2D textures.


### -field D3D10_RTV_DIMENSION_TEXTURE2DMS

The resource will be accessed as a 2D texture with multisampling.


### -field D3D10_RTV_DIMENSION_TEXTURE2DMSARRAY

The resource will be accessed as an array of 2D textures with multisampling.


### -field D3D10_RTV_DIMENSION_TEXTURE3D

The resource will be accessed as a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">3D texture</a>.


## -remarks



This enumeration is used in <a href="https://msdn.microsoft.com/05a8dcf3-c815-47f1-b51f-e382804b030b">D3D10_RENDER_TARGET_VIEW_DESC</a> to create a render-target view.




## -see-also




<a href="https://msdn.microsoft.com/c986b22c-2960-4571-98bc-028c9f41ec65">Resource Enumerations</a>
 

 

