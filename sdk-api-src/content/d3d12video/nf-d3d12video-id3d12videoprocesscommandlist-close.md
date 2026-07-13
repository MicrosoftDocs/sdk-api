---
UID: NF:d3d12video.ID3D12VideoProcessCommandList.Close
title: ID3D12VideoProcessCommandList::Close
description: Indicates that recording to the command list has finished. (ID3D12VideoProcessCommandList::Close)
helpviewer_keywords: ["ID3D12VideoProcessCommandList::Close","Close","ID3D12VideoProcessCommandList.Close","ID3D12VideoProcessCommandList::Close","ID3D12VideoProcessCommandList.Close"]
tech.root: mf
ms.assetid: 2d8a7a37-32b4-4fb0-b8db-d8460624aa63
ms.date: 05/28/2019
ms.keywords: ID3D12VideoProcessCommandList::Close, Close, ID3D12VideoProcessCommandList.Close, ID3D12VideoProcessCommandList::Close, ID3D12VideoProcessCommandList.Close
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
 - ID3D12VideoProcessCommandList::Close
 - d3d12video/ID3D12VideoProcessCommandList::Close
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoProcessCommandList::Close
---

# ID3D12VideoProcessCommandList::Close


## -description

Indicates that recording to the command list has finished.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the following values:
              

<ul>
<li><b>E_FAIL</b> if the command list has already been closed, or an invalid API was called during command list recording.
              </li>
<li><b>E_OUTOFMEMORY</b> if the operating system ran out of memory during recording.
              </li>
<li><b>E_INVALIDARG</b> if an invalid argument was passed to the command list API during recording.
              </li>
</ul>

See <a href="/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> for other possible return values.

## -remarks

The runtime will validate that the command list has not previously been closed.  If an error was encountered during recording, the error code is returned here.  The runtime won't call the close device driver interface (DDI) in this case.

For an example of creating a command list, see [ID3D12GraphicsCommandList::Close method](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)

## -see-also
