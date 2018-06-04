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
 

 

