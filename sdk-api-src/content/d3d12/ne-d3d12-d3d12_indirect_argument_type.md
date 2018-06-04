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

# D3D12_INDIRECT_ARGUMENT_TYPE enumeration


## -description



          Specifies the type of the indirect parameter.
        


## -enum-fields




### -field D3D12_INDIRECT_ARGUMENT_TYPE_DRAW

Indicates the type is a Draw call.


### -field D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INDEXED

Indicates the type is a DrawIndexed call.


### -field D3D12_INDIRECT_ARGUMENT_TYPE_DISPATCH

Indicates the type is a Dispatch call.


### -field D3D12_INDIRECT_ARGUMENT_TYPE_VERTEX_BUFFER_VIEW

Indicates the type is a vertex buffer view.


### -field D3D12_INDIRECT_ARGUMENT_TYPE_INDEX_BUFFER_VIEW

Indicates the type is an index buffer view.


### -field D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT

Indicates the type is a constant.


### -field D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT_BUFFER_VIEW

Indicates the type is a constant buffer view (CBV).


### -field D3D12_INDIRECT_ARGUMENT_TYPE_SHADER_RESOURCE_VIEW

Indicates the type is a shader resource view (SRV).


### -field D3D12_INDIRECT_ARGUMENT_TYPE_UNORDERED_ACCESS_VIEW

Indicates the type is an unordered access view (UAV).


## -remarks




          This enum is used by the <a href="https://msdn.microsoft.com/2B51E4B1-F48A-4937-A92D-6AE9449018B4">D3D12_INDIRECT_ARGUMENT_DESC</a> structure.
        




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

