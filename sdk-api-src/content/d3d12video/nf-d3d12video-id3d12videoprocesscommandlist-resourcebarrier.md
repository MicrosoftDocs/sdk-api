---
UID: NF:d3d12video.ID3D12VideoProcessCommandList.ResourceBarrier
title: ID3D12VideoProcessCommandList::ResourceBarrier
author: windows-sdk-content
description: Notifies the driver that it needs to synchronize multiple accesses to resources.
tech.root: mf
ms.assetid: 9c37e5aa-b9f7-4e72-ae08-cf0403d0bc5a
ms.author: windowssdkdev
ms.date: 05/28/2019
ms.topic: method
ms.keywords: ID3D12VideoProcessCommandList::ResourceBarrier, ResourceBarrier, ID3D12VideoProcessCommandList.ResourceBarrier, ID3D12VideoProcessCommandList::ResourceBarrier, ID3D12VideoProcessCommandList.ResourceBarrier
req.header: d3d12video.h
req.include-header:
req.redist:
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.lib:
req.dll: d3d12.dll
req.irql: 
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoProcessCommandList::ResourceBarrier
product: Windows
targetos: Windows

---

# ID3D12VideoProcessCommandList::ResourceBarrier


## -description

Notifies the driver that it needs to synchronize multiple accesses to resources.

## -parameters

### -param NumBarriers

Type: <b>UINT</b>

The number of submitted barrier descriptions.

### -param pBarriers

Type: <b>const <a href="https://msdn.microsoft.com/49F02D65-767E-4BA4-A90D-68AA2D709E09">D3D12_RESOURCE_BARRIER</a>*</b>

Pointer to an array of barrier descriptions.
          

## -returns

This method returns void.

## -remarks

## -see-also