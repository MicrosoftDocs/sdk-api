---
UID: NS:d3d12.D3D12_SUBRESOURCE_DATA
title: D3D12_SUBRESOURCE_DATA
author: windows-driver-content
description: Describes subresource data.
old-location: direct3d12\d3d12_subresource_data.htm
old-project: direct3d12
ms.assetid: A2749C3A-FD61-4775-8727-2D1CFC79A0F8
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: D3D12_SUBRESOURCE_DATA, D3D12_SUBRESOURCE_DATA structure, d3d12/D3D12_SUBRESOURCE_DATA, direct3d12.d3d12_subresource_data
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D12_SUBRESOURCE_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D12.h
api_name:
-	D3D12_SUBRESOURCE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_SUBRESOURCE_DATA structure


## -description



        Describes subresource data.
      


## -struct-fields




### -field pData


            A pointer to a memory block that contains the subresource data.
          


### -field RowPitch


            The row pitch, or width, or physical size, in bytes, of the subresource data.
          


### -field SlicePitch


            The depth pitch, or width, or physical size, in bytes, of the subresource data.
          


## -remarks



This structure is used by a number of the helper functions, refer to <a href="https://msdn.microsoft.com/095958A9-345B-45AE-8363-B353534044B2">Helper Structures and Functions for D3D12</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

