---
UID: NF:d3d12.ID3D12CommandQueue.GetTimestampFrequency
title: ID3D12CommandQueue::GetTimestampFrequency (d3d12.h)
description: This method is used to determine the rate at which the GPU timestamp counter increments.
helpviewer_keywords: ["GetTimestampFrequency","GetTimestampFrequency method","GetTimestampFrequency method","ID3D12CommandQueue interface","ID3D12CommandQueue interface","GetTimestampFrequency method","ID3D12CommandQueue.GetTimestampFrequency","ID3D12CommandQueue::GetTimestampFrequency","d3d12/ID3D12CommandQueue::GetTimestampFrequency","direct3d12.id3d12commandqueue_gettimestampfrequency"]
old-location: direct3d12\id3d12commandqueue_gettimestampfrequency.htm
tech.root: direct3d12
ms.assetid: 90D79775-2898-453E-87FB-CD6850829E47
ms.date: 12/05/2018
ms.keywords: GetTimestampFrequency, GetTimestampFrequency method, GetTimestampFrequency method,ID3D12CommandQueue interface, ID3D12CommandQueue interface,GetTimestampFrequency method, ID3D12CommandQueue.GetTimestampFrequency, ID3D12CommandQueue::GetTimestampFrequency, d3d12/ID3D12CommandQueue::GetTimestampFrequency, direct3d12.id3d12commandqueue_gettimestampfrequency
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
 - ID3D12CommandQueue::GetTimestampFrequency
 - d3d12/ID3D12CommandQueue::GetTimestampFrequency
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
 - ID3D12CommandQueue.GetTimestampFrequency
---

# ID3D12CommandQueue::GetTimestampFrequency


## -description

This method is used to determine the rate at which the GPU timestamp counter increments.

## -parameters

### -param pFrequency [out]

Type: <b>UINT64*</b>

The GPU timestamp counter frequency (in ticks/second).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

For more information, refer to <a href="/windows/desktop/direct3d12/timing">Timing</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue">ID3D12CommandQueue</a>