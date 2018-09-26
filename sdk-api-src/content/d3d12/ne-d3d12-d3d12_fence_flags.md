---
UID: NE:d3d12.D3D12_FENCE_FLAGS
title: D3D12_FENCE_FLAGS
author: windows-sdk-content
description: Specifies fence options.
old-location: direct3d12\d3d12_fence_flags.htm
tech.root: direct3d12
ms.assetid: EF725566-B77A-40EE-B5E3-86C5D13CC7D5
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: D3D12_FENCE_FLAGS, D3D12_FENCE_FLAGS enumeration, D3D12_FENCE_FLAG_NONE, D3D12_FENCE_FLAG_NON_MONITORED, D3D12_FENCE_FLAG_SHARED, D3D12_FENCE_FLAG_SHARED_CROSS_ADAPTER, d3d12/D3D12_FENCE_FLAGS, d3d12/D3D12_FENCE_FLAG_NONE, d3d12/D3D12_FENCE_FLAG_NON_MONITORED, d3d12/D3D12_FENCE_FLAG_SHARED, d3d12/D3D12_FENCE_FLAG_SHARED_CROSS_ADAPTER, direct3d12.d3d12_fence_flags
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FENCE_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_FENCE_FLAGS
req.redist: 
---

# D3D12_FENCE_FLAGS enumeration


## -description


Specifies fence options.
        


## -enum-fields




### -field D3D12_FENCE_FLAG_NONE

No options are specified.
          


### -field D3D12_FENCE_FLAG_SHARED

The fence is shared.
          


### -field D3D12_FENCE_FLAG_SHARED_CROSS_ADAPTER

The fence is shared with another GPU adapter.
          


### -field D3D12_FENCE_FLAG_NON_MONITORED

The fence is of the non-monitored type. Non-monitored fences should only be used when the adapter doesn't support monitored fences, or when a fence is shared with an adapter that doesn't support monitored fences.
          


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/731A60CA-644A-4FC2-8461-DDD686363BED">ID3D12Device::CreateFence</a> method.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

