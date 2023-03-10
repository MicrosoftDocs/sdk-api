---
UID: NF:d3d12video.ID3D12VideoEncodeCommandList.ResourceBarrier
title: ID3D12VideoEncodeCommandList::ResourceBarrier
ms.date: 11/4/2019
targetos: Windows
description: Notifies the driver that it needs to synchronize multiple accesses to resources. (ID3D12VideoEncodeCommandList::ResourceBarrier)
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: d3d12.dll
req.header: d3d12video.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoEncodeCommandList::ResourceBarrier
f1_keywords:
 - ID3D12VideoEncodeCommandList::ResourceBarrier
 - d3d12video/ID3D12VideoEncodeCommandList::ResourceBarrier
dev_langs:
 - c++
---

## -description

Notifies the driver that it needs to synchronize multiple accesses to resources.

## -parameters

### -param NumBarriers

Type: <b>UINT</b>

The number of submitted barrier descriptions.

### -param pBarriers

Type: <b>const <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier">D3D12_RESOURCE_BARRIER</a>*</b>

Pointer to an array of barrier descriptions.

## -remarks

This method returns void.

## -see-also
