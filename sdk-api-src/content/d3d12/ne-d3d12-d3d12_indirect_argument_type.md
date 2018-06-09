---
UID: NE:d3d12.D3D12_INDIRECT_ARGUMENT_TYPE
title: D3D12_INDIRECT_ARGUMENT_TYPE
author: windows-sdk-content
description: Specifies the type of the indirect parameter.
old-location: direct3d12\d3d12_indirect_argument_type.htm
old-project: direct3d12
ms.assetid: 03324A50-BE16-4FC0-BFE7-9EE97C738165
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: D3D12_INDIRECT_ARGUMENT_TYPE, D3D12_INDIRECT_ARGUMENT_TYPE enumeration, D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT, D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT_BUFFER_VIEW, D3D12_INDIRECT_ARGUMENT_TYPE_DISPATCH, D3D12_INDIRECT_ARGUMENT_TYPE_DRAW, D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INDEXED, D3D12_INDIRECT_ARGUMENT_TYPE_INDEX_BUFFER_VIEW, D3D12_INDIRECT_ARGUMENT_TYPE_SHADER_RESOURCE_VIEW, D3D12_INDIRECT_ARGUMENT_TYPE_UNORDERED_ACCESS_VIEW, D3D12_INDIRECT_ARGUMENT_TYPE_VERTEX_BUFFER_VIEW, d3d12/D3D12_INDIRECT_ARGUMENT_TYPE, d3d12/D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT, d3d12/D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT_BUFFER_VIEW, d3d12/D3D12_INDIRECT_ARGUMENT_TYPE_DISPATCH, d3d12/D3D12_INDIRECT_ARGUMENT_TYPE_DRAW, d3d12/D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INDEXED, d3d12/D3D12_INDIRECT_ARGUMENT_TYPE_INDEX_BUFFER_VIEW, d3d12/D3D12_INDIRECT_ARGUMENT_TYPE_SHADER_RESOURCE_VIEW, d3d12/D3D12_INDIRECT_ARGUMENT_TYPE_UNORDERED_ACCESS_VIEW, d3d12/D3D12_INDIRECT_ARGUMENT_TYPE_VERTEX_BUFFER_VIEW, direct3d12.d3d12_indirect_argument_type
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
tech.root: 
req.typenames: D3D12_INDIRECT_ARGUMENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_INDIRECT_ARGUMENT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

