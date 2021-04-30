---
UID: NF:dxgi1_4.IDXGIAdapter3.QueryVideoMemoryInfo
title: IDXGIAdapter3::QueryVideoMemoryInfo (dxgi1_4.h)
description: This method informs the process of the current budget and process usage.
helpviewer_keywords: ["IDXGIAdapter3 interface [DXGI]","QueryVideoMemoryInfo method","IDXGIAdapter3.QueryVideoMemoryInfo","IDXGIAdapter3::QueryVideoMemoryInfo","QueryVideoMemoryInfo","QueryVideoMemoryInfo method [DXGI]","QueryVideoMemoryInfo method [DXGI]","IDXGIAdapter3 interface","direct3ddxgi.idxgiadapter3_queryvideomemoryinfo","dxgi1_4/IDXGIAdapter3::QueryVideoMemoryInfo"]
old-location: direct3ddxgi\idxgiadapter3_queryvideomemoryinfo.htm
tech.root: direct3ddxgi
ms.assetid: A2F95FE5-CF8D-4F17-8CC8-62AAA40B71FC
ms.date: 12/05/2018
ms.keywords: IDXGIAdapter3 interface [DXGI],QueryVideoMemoryInfo method, IDXGIAdapter3.QueryVideoMemoryInfo, IDXGIAdapter3::QueryVideoMemoryInfo, QueryVideoMemoryInfo, QueryVideoMemoryInfo method [DXGI], QueryVideoMemoryInfo method [DXGI],IDXGIAdapter3 interface, direct3ddxgi.idxgiadapter3_queryvideomemoryinfo, dxgi1_4/IDXGIAdapter3::QueryVideoMemoryInfo
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
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIAdapter3::QueryVideoMemoryInfo
 - dxgi1_4/IDXGIAdapter3::QueryVideoMemoryInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIAdapter3.QueryVideoMemoryInfo
---

# IDXGIAdapter3::QueryVideoMemoryInfo


## -description

This method informs the process of the current budget and process usage.

## -parameters

### -param NodeIndex [in]

Type: <b>UINT</b>

Specifies the device's physical adapter for which the video memory information is queried.
            For single-GPU operation, set this to zero.
            If there are multiple GPU nodes, set this to the index of the node (the device's physical adapter) for which the video memory information is queried.
            See <a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>.

### -param MemorySegmentGroup [in]

Type: <b><a href="/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group">DXGI_MEMORY_SEGMENT_GROUP</a></b>

Specifies a DXGI_MEMORY_SEGMENT_GROUP that identifies the group as local or non-local.

### -param pVideoMemoryInfo [out]

Type: <b><a href="/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info">DXGI_QUERY_VIDEO_MEMORY_INFO</a>*</b>

Fills in a DXGI_QUERY_VIDEO_MEMORY_INFO structure with the current values.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; an error code otherwise.
            For a list of error codes, see <a href="/windows/win32/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

Applications must explicitly manage their usage of physical memory explicitly and keep usage within the budget assigned to the application process.
          Processes that cannot kept their usage within their assigned budgets will likely experience stuttering, as they are intermittently frozen and paged-out to allow other processes to run.

## -see-also

<a href="/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3">IDXGIAdapter3</a>

