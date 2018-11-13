---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetComputeRoot32BitConstant
title: ID3D12GraphicsCommandList::SetComputeRoot32BitConstant
author: windows-sdk-content
description: Sets a constant in the compute root signature.
old-location: direct3d12\id3d12graphicscommandlist_setcomputeroot32bitconstant.htm
tech.root: direct3d12
ms.assetid: A250052F-A24A-4234-8A39-0995A00B6E01
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetComputeRoot32BitConstant method, ID3D12GraphicsCommandList.SetComputeRoot32BitConstant, ID3D12GraphicsCommandList::SetComputeRoot32BitConstant, SetComputeRoot32BitConstant, SetComputeRoot32BitConstant method, SetComputeRoot32BitConstant method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetComputeRoot32BitConstant, direct3d12.id3d12graphicscommandlist_setcomputeroot32bitconstant
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
 - ID3D12GraphicsCommandList.SetComputeRoot32BitConstant
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::SetComputeRoot32BitConstant


## -description


Sets a constant in the compute root signature.
        


## -parameters




### -param RootParameterIndex [in]

Type: <b>UINT</b>

The slot number for binding.
          


### -param SrcData [in]

Type: <b>UINT</b>

The source data for the constant to set.
          


### -param DestOffsetIn32BitValues [in]

Type: <b>UINT</b>

The offset, in 32-bit values, to set the constant in the root signature.
          


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

