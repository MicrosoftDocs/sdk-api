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

# D3D11_RESOURCE_DIMENSION enumeration


## -description


Identifies the type of resource being used.


## -enum-fields




### -field D3D11_RESOURCE_DIMENSION_UNKNOWN

Resource is of unknown type.


### -field D3D11_RESOURCE_DIMENSION_BUFFER

Resource is a buffer.


### -field D3D11_RESOURCE_DIMENSION_TEXTURE1D

Resource is a 1D texture.


### -field D3D11_RESOURCE_DIMENSION_TEXTURE2D

Resource is a 2D texture.


### -field D3D11_RESOURCE_DIMENSION_TEXTURE3D

Resource is a 3D texture.


## -remarks



This enumeration is used in <a href="https://msdn.microsoft.com/8358ab9b-acf3-41cd-8812-cc15862928da">ID3D11Resource::GetType</a>. 




## -see-also




<a href="https://msdn.microsoft.com/b547819b-7006-40b5-84a4-adf198048051">Resource Enumerations</a>
 

 

