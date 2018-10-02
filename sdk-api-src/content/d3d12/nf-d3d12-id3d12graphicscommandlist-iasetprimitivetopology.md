---
UID: NF:d3d12.ID3D12GraphicsCommandList.IASetPrimitiveTopology
title: ID3D12GraphicsCommandList::IASetPrimitiveTopology
author: windows-sdk-content
description: Bind information about the primitive type, and data order that describes input data for the input assembler stage.
old-location: direct3d12\id3d12graphicscommandlist_iasetprimitivetopology.htm
tech.root: direct3d12
ms.assetid: 743C48DF-C67E-48A0-B027-B2776E65968F
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: IASetPrimitiveTopology, IASetPrimitiveTopology method, IASetPrimitiveTopology method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,IASetPrimitiveTopology method, ID3D12GraphicsCommandList.IASetPrimitiveTopology, ID3D12GraphicsCommandList::IASetPrimitiveTopology, d3d12/ID3D12GraphicsCommandList::IASetPrimitiveTopology, direct3d12.id3d12graphicscommandlist_iasetprimitivetopology
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::IASetPrimitiveTopology


## -description


Bind information about the primitive type, and data order that describes input data for the input assembler stage.


## -parameters




### -param PrimitiveTopology [in]

Type: <b>D3D12_PRIMITIVE_TOPOLOGY</b>

The type of primitive and ordering of the primitive data (see <a href="https://msdn.microsoft.com/b4becdcc-cc19-4d5a-940b-b232ebedce68">D3D_PRIMITIVE_TOPOLOGY</a>).
          


## -returns



This method does not return a value.
          




## -see-also




<a href="https://msdn.microsoft.com/3BD4DF5E-EA91-4B2A-AADE-B9AE0E766F63">D3D12_PRIMITIVE_TOPOLOGY_TYPE</a>



<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

