---
UID: NF:d3d12.ID3D12Fence.SetEventOnCompletion
title: ID3D12Fence::SetEventOnCompletion (d3d12.h)
description: Specifies an event that should be fired when the fence reaches a certain value.
helpviewer_keywords: ["ID3D12Fence interface","SetEventOnCompletion method","ID3D12Fence.SetEventOnCompletion","ID3D12Fence::SetEventOnCompletion","SetEventOnCompletion","SetEventOnCompletion method","SetEventOnCompletion method","ID3D12Fence interface","d3d12/ID3D12Fence::SetEventOnCompletion","direct3d12.id3d12fence_seteventoncompletion"]
old-location: direct3d12\id3d12fence_seteventoncompletion.htm
tech.root: direct3d12
ms.assetid: DBC5A1FD-F3D0-4C9B-965B-1967151093F7
ms.date: 12/05/2018
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
 - ID3D12Fence::SetEventOnCompletion
 - d3d12/ID3D12Fence::SetEventOnCompletion
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
 - ID3D12Fence.SetEventOnCompletion
---

## -description

Specifies an event that's raised when the fence reaches a certain value.

## -parameters

### -param Value

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT64</a></b>

The fence value when the event is to be signaled.

### -param hEvent

Type: <b><a href="/windows/win32/WinProg/windows-data-types">HANDLE</a></b>

A handle to the event object.

## -returns

Type: <b>HRESULT</b>

This method returns <b>E_OUTOFMEMORY</b> if the kernel components don’t have sufficient memory to store the event in a list. See <a href="/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 return codes</a> for other possible return values.

## -remarks

To specify multiple fences before an event is triggered, refer to <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion">SetEventOnMultipleFenceCompletion</a>.

If *hEvent* is a null handle, then this API will not return until the specified fence value(s) have been reached.

This method can be safely called from multiple threads at one time.

## Examples

The <a href="/windows/win32/direct3d12/working-samples">D3D12Multithreading</a> sample uses <b>ID3D12Fence::SetEventOnCompletion</b> as follows:

```cpp
// Wait for the command list to execute; we are reusing the same command 
// list in our main loop but for now, we just want to wait for setup to 
// complete before continuing.

// Signal and increment the fence value.
const UINT64 fenceToWaitFor = m_fenceValue;
ThrowIfFailed(m_commandQueue->Signal(m_fence.Get(), fenceToWaitFor));
m_fenceValue++;

// Wait until the fence is completed.
ThrowIfFailed(m_fence->SetEventOnCompletion(fenceToWaitFor, m_fenceEvent));
WaitForSingleObject(m_fenceEvent, INFINITE);
```

Refer to the <a href="/windows/win32/direct3d12/notes-on-example-code">Example code in the Direct3D 12 reference</a>.

## -see-also

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>

<a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>

