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
 

 

