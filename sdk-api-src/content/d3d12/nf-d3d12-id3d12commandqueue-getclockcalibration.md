---
UID: NF:d3d12.ID3D12CommandQueue.GetClockCalibration
title: ID3D12CommandQueue::GetClockCalibration (d3d12.h)
description: This method samples the CPU and GPU timestamp counters at the same moment in time.
helpviewer_keywords: ["GetClockCalibration","GetClockCalibration method","GetClockCalibration method","ID3D12CommandQueue interface","ID3D12CommandQueue interface","GetClockCalibration method","ID3D12CommandQueue.GetClockCalibration","ID3D12CommandQueue::GetClockCalibration","d3d12/ID3D12CommandQueue::GetClockCalibration","direct3d12.id3d12commandqueue_getclockcalibration"]
old-location: direct3d12\id3d12commandqueue_getclockcalibration.htm
tech.root: direct3d12
ms.assetid: B8E0F8D4-D291-41B5-8E40-0C1FB3DCC253
ms.date: 12/05/2018
ms.keywords: GetClockCalibration, GetClockCalibration method, GetClockCalibration method,ID3D12CommandQueue interface, ID3D12CommandQueue interface,GetClockCalibration method, ID3D12CommandQueue.GetClockCalibration, ID3D12CommandQueue::GetClockCalibration, d3d12/ID3D12CommandQueue::GetClockCalibration, direct3d12.id3d12commandqueue_getclockcalibration
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12CommandQueue::GetClockCalibration
 - d3d12/ID3D12CommandQueue::GetClockCalibration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12CommandQueue.GetClockCalibration
---

# ID3D12CommandQueue::GetClockCalibration


## -description

This method samples the CPU and GPU timestamp counters at the same moment in time.

## -parameters

### -param pGpuTimestamp [out]

Type: <b>UINT64*</b>

The value of the GPU timestamp counter.

### -param pCpuTimestamp [out]

Type: <b>UINT64*</b>

The value of the CPU timestamp counter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

For more information, refer to <a href="/windows/desktop/direct3d12/timing">Timing</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue">ID3D12CommandQueue</a>