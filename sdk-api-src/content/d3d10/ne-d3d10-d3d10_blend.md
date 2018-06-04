---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D10_BLEND enumeration


## -description


Blend options. A blend option identifies the data source and an optional pre-blend operation.


## -enum-fields




### -field D3D10_BLEND_ZERO

The data source is the color black (0, 0, 0, 0). No pre-blend operation.


### -field D3D10_BLEND_ONE

The data source is the color white (1, 1, 1, 1). No pre-blend operation.


### -field D3D10_BLEND_SRC_COLOR

The data source is color data (RGB) from a pixel shader. No pre-blend operation.


### -field D3D10_BLEND_INV_SRC_COLOR

The data source is color data (RGB) from a pixel shader. The pre-blend operation inverts the data, generating 1 - RGB.


### -field D3D10_BLEND_SRC_ALPHA

The data source is alpha data (A) from a pixel shader. No pre-blend operation.


### -field D3D10_BLEND_INV_SRC_ALPHA

The data source is alpha data (A) from a pixel shader. The pre-blend operation inverts the data, generating 1 - A.


### -field D3D10_BLEND_DEST_ALPHA

The data source is alpha data from a rendertarget. No pre-blend operation.


### -field D3D10_BLEND_INV_DEST_ALPHA

The data source is alpha data from a rendertarget. The pre-blend operation inverts the data, generating 1 - A.


### -field D3D10_BLEND_DEST_COLOR

The data source is color data from a rendertarget. No pre-blend operation.


### -field D3D10_BLEND_INV_DEST_COLOR

The data source is color data from a rendertarget. The pre-blend operation inverts the data, generating 1 - RGB.


### -field D3D10_BLEND_SRC_ALPHA_SAT

The data source is alpha data from a pixel shader. The pre-blend operation clamps the data to 1 or less. 



### -field D3D10_BLEND_BLEND_FACTOR

The data source is the blend factor set with <a href="https://msdn.microsoft.com/39169f4f-8a7b-4db0-abd5-5b67b204b394">ID3D10Device::OMSetBlendState</a>. No pre-blend operation.


### -field D3D10_BLEND_INV_BLEND_FACTOR

The data source is the blend factor set with <a href="https://msdn.microsoft.com/39169f4f-8a7b-4db0-abd5-5b67b204b394">ID3D10Device::OMSetBlendState</a>. The pre-blend operation inverts the blend factor, generating 1 - blend_factor.


### -field D3D10_BLEND_SRC1_COLOR

The data sources are both color data output by a pixel shader. There is no pre-blend operation. This options supports <a href="https://msdn.microsoft.com/f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3">dual-source color blending</a>.


### -field D3D10_BLEND_INV_SRC1_COLOR

The data sources are both color data output by a pixel shader. The pre-blend operation inverts the data, generating 1 - RGB. This options supports <a href="https://msdn.microsoft.com/f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3">dual-source color blending</a>.


### -field D3D10_BLEND_SRC1_ALPHA

The data sources are alpha data output by a pixel shader. There is no pre-blend operation. This options supports <a href="https://msdn.microsoft.com/f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3">dual-source color blending</a>.


### -field D3D10_BLEND_INV_SRC1_ALPHA

The data sources are alpha data output by a pixel shader. The pre-blend operation inverts the data, generating 1 - A. This options supports <a href="https://msdn.microsoft.com/f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3">dual-source color blending</a>.


## -remarks



Blend operations are specified in a <a href="https://msdn.microsoft.com/c256dd1e-2b25-4dc5-8e49-5bf2b419b3c5">blend description</a>.




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

