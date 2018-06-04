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
 

 

