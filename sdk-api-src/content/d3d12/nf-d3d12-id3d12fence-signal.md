---
UID: NF:d3d12.ID3D12Fence.Signal
title: ID3D12Fence::Signal (d3d12.h)
description: Sets the fence to the specified value.
helpviewer_keywords: ["ID3D12Fence interface","Signal method","ID3D12Fence.Signal","ID3D12Fence::Signal","Signal","Signal method","Signal method","ID3D12Fence interface","d3d12/ID3D12Fence::Signal","direct3d12.id3d12fence_signal"]
old-location: direct3d12\id3d12fence_signal.htm
tech.root: direct3d12
ms.assetid: 8AC955C1-37C9-47F3-B35C-980783C58390
ms.date: 12/05/2018
ms.keywords: ID3D12Fence interface,Signal method, ID3D12Fence.Signal, ID3D12Fence::Signal, Signal, Signal method, Signal method,ID3D12Fence interface, d3d12/ID3D12Fence::Signal, direct3d12.id3d12fence_signal
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Fence::Signal
 - d3d12/ID3D12Fence::Signal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Fence.Signal
---

# ID3D12Fence::Signal


## -description

Sets the fence to the specified value.

## -parameters

### -param Value

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT64</a></b>

The value to set the fence to.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

Use this method to set a fence value from the CPU side. Use <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal">ID3D12CommandQueue::Signal</a> to set a fence from the GPU side.

## -see-also

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>



<a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>

