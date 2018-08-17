---
UID: NF:d3d12.ID3D12GraphicsCommandList.IASetPrimitiveTopology
title: ID3D12GraphicsCommandList::IASetPrimitiveTopology
author: windows-sdk-content
description: Bind information about the primitive type, and data order that describes input data for the input assembler stage.
old-location: direct3d12\id3d12graphicscommandlist_iasetprimitivetopology.htm
old-project: direct3d12
ms.assetid: 743C48DF-C67E-48A0-B027-B2776E65968F
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IASetPrimitiveTopology, IASetPrimitiveTopology method, IASetPrimitiveTopology method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,IASetPrimitiveTopology method, ID3D12GraphicsCommandList.IASetPrimitiveTopology, ID3D12GraphicsCommandList::IASetPrimitiveTopology, d3d12/ID3D12GraphicsCommandList::IASetPrimitiveTopology, direct3d12.id3d12graphicscommandlist_iasetprimitivetopology
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12.h
req.include-header: 
req.redist: 
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
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.IASetPrimitiveTopology
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::IASetPrimitiveTopology


## -description


Bind information about the primitive type, and data order that describes input data for the input assembler stage.


## -parameters




### -param PrimitiveTopology [in]

Type: <b>D3D12_PRIMITIVE_TOPOLOGY</b>

The type of primitive and ordering of the primitive data (see <a href="https://msdn.microsoft.com/en-us/library/Ff728726(v=VS.85).aspx">D3D_PRIMITIVE_TOPOLOGY</a>).
          


## -returns



This method does not return a value.
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn770385(v=VS.85).aspx">D3D12_PRIMITIVE_TOPOLOGY_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn903537(v=VS.85).aspx">ID3D12GraphicsCommandList</a>
 

 

