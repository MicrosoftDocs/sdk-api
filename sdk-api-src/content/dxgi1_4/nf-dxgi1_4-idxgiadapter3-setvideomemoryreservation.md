---
UID: NF:dxgi1_4.IDXGIAdapter3.SetVideoMemoryReservation
title: IDXGIAdapter3::SetVideoMemoryReservation (dxgi1_4.h)
description: This method sends the minimum required physical memory for an application, to the OS.
helpviewer_keywords: ["IDXGIAdapter3 interface [DXGI]","SetVideoMemoryReservation method","IDXGIAdapter3.SetVideoMemoryReservation","IDXGIAdapter3::SetVideoMemoryReservation","SetVideoMemoryReservation","SetVideoMemoryReservation method [DXGI]","SetVideoMemoryReservation method [DXGI]","IDXGIAdapter3 interface","direct3ddxgi.idxgiadapter3_setvideomemoryreservation","dxgi1_4/IDXGIAdapter3::SetVideoMemoryReservation"]
old-location: direct3ddxgi\idxgiadapter3_setvideomemoryreservation.htm
tech.root: direct3ddxgi
ms.assetid: 5D17F57F-9FFA-4B5C-98B6-33E5B3982A63
ms.date: 12/05/2018
ms.keywords: IDXGIAdapter3 interface [DXGI],SetVideoMemoryReservation method, IDXGIAdapter3.SetVideoMemoryReservation, IDXGIAdapter3::SetVideoMemoryReservation, SetVideoMemoryReservation, SetVideoMemoryReservation method [DXGI], SetVideoMemoryReservation method [DXGI],IDXGIAdapter3 interface, direct3ddxgi.idxgiadapter3_setvideomemoryreservation, dxgi1_4/IDXGIAdapter3::SetVideoMemoryReservation
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
 - IDXGIAdapter3::SetVideoMemoryReservation
 - dxgi1_4/IDXGIAdapter3::SetVideoMemoryReservation
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
 - IDXGIAdapter3.SetVideoMemoryReservation
---

# IDXGIAdapter3::SetVideoMemoryReservation


## -description

This method sends the minimum required physical memory for an application, to the OS.

## -parameters

### -param NodeIndex [in]

Type: <b>UINT</b>

Specifies the device's physical adapter for which the video memory information is being set.
            For single-GPU operation, set this to zero.
            If there are multiple GPU nodes, set this to the index of the node (the device's physical adapter) for which the video memory information is being set.
            See <a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>.

### -param MemorySegmentGroup [in]

Type: <b><a href="/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group">DXGI_MEMORY_SEGMENT_GROUP</a></b>

Specifies a DXGI_MEMORY_SEGMENT_GROUP that identifies the group as local or non-local.

### -param Reservation [in]

Type: <b>UINT64</b>

Specifies a UINT64 that sets the minimum required physical memory, in bytes.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; an error code otherwise.
            For a list of error codes, see <a href="/windows/win32/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

Applications are encouraged to set a video reservation to denote the amount of physical memory they cannot go without.
          This value helps the OS quickly minimize the impact of large memory pressure situations.

## -see-also

<a href="/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3">IDXGIAdapter3</a>

