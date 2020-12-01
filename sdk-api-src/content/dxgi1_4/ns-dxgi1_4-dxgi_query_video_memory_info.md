---
UID: NS:dxgi1_4.DXGI_QUERY_VIDEO_MEMORY_INFO
title: DXGI_QUERY_VIDEO_MEMORY_INFO (dxgi1_4.h)
description: Describes the current video memory budgeting parameters.
helpviewer_keywords: ["DXGI_QUERY_VIDEO_MEMORY_INFO","DXGI_QUERY_VIDEO_MEMORY_INFO structure [DXGI]","direct3ddxgi.dxgi_query_video_memory_info","dxgi1_4/DXGI_QUERY_VIDEO_MEMORY_INFO"]
old-location: direct3ddxgi\dxgi_query_video_memory_info.htm
tech.root: direct3ddxgi
ms.assetid: E710F3A9-CB12-43B0-B56C-789350BCAE59
ms.date: 12/05/2018
ms.keywords: DXGI_QUERY_VIDEO_MEMORY_INFO, DXGI_QUERY_VIDEO_MEMORY_INFO structure [DXGI], direct3ddxgi.dxgi_query_video_memory_info, dxgi1_4/DXGI_QUERY_VIDEO_MEMORY_INFO
req.header: dxgi1_4.h
req.include-header: DXGI1_3.h
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
targetos: Windows
req.typenames: DXGI_QUERY_VIDEO_MEMORY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_QUERY_VIDEO_MEMORY_INFO
 - dxgi1_4/DXGI_QUERY_VIDEO_MEMORY_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_4.h
api_name:
 - DXGI_QUERY_VIDEO_MEMORY_INFO
---

# DXGI_QUERY_VIDEO_MEMORY_INFO structure


## -description

Describes the current video memory budgeting parameters.

## -struct-fields

### -field Budget

Specifies the OS-provided video memory budget, in bytes, that the application should target. If <i>CurrentUsage</i> is greater than <i>Budget</i>, the application may incur stuttering or performance penalties due to background activity by the OS to provide other applications with a fair usage of video memory.

### -field CurrentUsage

              Specifies the application’s current video memory usage, in bytes.

### -field AvailableForReservation

              The amount of video memory, in bytes, that the application has available for reservation. To reserve this video memory, the application should call <a href="/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-setvideomemoryreservation">IDXGIAdapter3::SetVideoMemoryReservation</a>.

### -field CurrentReservation

              The amount of video memory, in bytes, that is reserved by the application. The OS uses the reservation as a hint to determine the application’s minimum working set. Applications should attempt to ensure that their video memory usage can be trimmed to meet this requirement.

## -remarks

Use this structure with <a href="/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo">QueryVideoMemoryInfo</a>.

Refer to the remarks for <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool">D3D12_MEMORY_POOL</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>