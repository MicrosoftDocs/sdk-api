---
UID: NF:d3d12video.ID3D12VideoProcessCommandList.Reset
title: ID3D12VideoProcessCommandList::Reset
description: Resets a command list back to its initial state as if a new command list was just created. (ID3D12VideoProcessCommandList::Reset)
helpviewer_keywords: ["ID3D12VideoProcessCommandList::Reset","Reset","ID3D12VideoProcessCommandList.Reset","ID3D12VideoProcessCommandList::Reset","ID3D12VideoProcessCommandList.Reset"]
tech.root: mf
ms.assetid: 95ddb93d-313e-48a3-ac09-e4675b4a1cad
ms.date: 05/28/2019
ms.keywords: ID3D12VideoProcessCommandList::Reset, Reset, ID3D12VideoProcessCommandList.Reset, ID3D12VideoProcessCommandList::Reset, ID3D12VideoProcessCommandList.Reset
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
targetos: Windows
f1_keywords:
 - ID3D12VideoProcessCommandList::Reset
 - d3d12video/ID3D12VideoProcessCommandList::Reset
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoProcessCommandList::Reset
---

# ID3D12VideoProcessCommandList::Reset


## -description

Resets a command list back to its initial state as if a new command list was just created.

## -parameters

### -param pAllocator

Type: <b>ID3D12CommandAllocator*</b>

A pointer to the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator">ID3D12CommandAllocator</a> object that the device creates command lists from.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the following values:
              

<ul>
<li><b>E_FAIL</b> if the command list was not in the "closed" state when the <b>Reset</b> call was made, or the per-device limit would have been exceeded.
              </li>
<li><b>E_OUTOFMEMORY</b> if the operating system ran out of memory.
              </li>
<li><b>E_INVALIDARG</b> if the allocator is currently being used with another command list in the "recording" state or if the specified allocator was created with the wrong type.
              </li>
</ul>
See <a href="/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> for other possible return values.

## -remarks

For additional information and examples of using this method, see [ID3D12GraphicsCommandList::Reset method](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)

## -see-also
