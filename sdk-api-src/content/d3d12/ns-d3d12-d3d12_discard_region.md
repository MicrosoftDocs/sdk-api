---
UID: NS:d3d12.D3D12_DISCARD_REGION
title: D3D12_DISCARD_REGION
author: windows-sdk-content
description: Describes details for the discard-resource operation.
old-location: direct3d12\d3d12_discard_region.htm
old-project: direct3d12
ms.assetid: 8F0916CB-3389-40BC-8028-BA8CF9BC566B
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: D3D12_DISCARD_REGION, D3D12_DISCARD_REGION structure, d3d12/D3D12_DISCARD_REGION, direct3d12.d3d12_discard_region
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: D3D12_DISCARD_REGION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_DISCARD_REGION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_DISCARD_REGION structure


## -description


Describes details for the discard-resource operation.
        


## -struct-fields




### -field NumRects

The number of rectangles in the array that the <b>pRects</b> member specifies.
          


### -field pRects

An array of <b>D3D12_RECT</b> structures for the rectangles in the resource to discard.
            If <b>NULL</b>, <a href="https://msdn.microsoft.com/2F4DBA5B-F586-4126-8867-BEE650F6D161">DiscardResource</a> discards the entire resource.
          


### -field FirstSubresource

Index of the first subresource in the resource to discard.
          


### -field NumSubresources

The number of subresources in the resource to discard.
          


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/2F4DBA5B-F586-4126-8867-BEE650F6D161">ID3D12GraphicsCommandList::DiscardResource</a> method.
      

If rectangles are supplied in this structure, the resource must have 2D subresources with all specified subresources the same dimension.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

