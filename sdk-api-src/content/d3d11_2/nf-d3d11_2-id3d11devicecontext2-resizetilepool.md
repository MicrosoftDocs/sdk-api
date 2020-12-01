---
UID: NF:d3d11_2.ID3D11DeviceContext2.ResizeTilePool
title: ID3D11DeviceContext2::ResizeTilePool (d3d11_2.h)
description: Resizes a tile pool.
helpviewer_keywords: ["ID3D11DeviceContext2 interface [Direct3D 11]","ResizeTilePool method","ID3D11DeviceContext2.ResizeTilePool","ID3D11DeviceContext2::ResizeTilePool","ResizeTilePool","ResizeTilePool method [Direct3D 11]","ResizeTilePool method [Direct3D 11]","ID3D11DeviceContext2 interface","d3d11_2/ID3D11DeviceContext2::ResizeTilePool","direct3d11.id3d11devicecontext2_resizetilepool"]
old-location: direct3d11\id3d11devicecontext2_resizetilepool.htm
tech.root: direct3d11
ms.assetid: 0F464025-7BF3-47C4-BD77-B4C312E53B07
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext2 interface [Direct3D 11],ResizeTilePool method, ID3D11DeviceContext2.ResizeTilePool, ID3D11DeviceContext2::ResizeTilePool, ResizeTilePool, ResizeTilePool method [Direct3D 11], ResizeTilePool method [Direct3D 11],ID3D11DeviceContext2 interface, d3d11_2/ID3D11DeviceContext2::ResizeTilePool, direct3d11.id3d11devicecontext2_resizetilepool
req.header: d3d11_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext2::ResizeTilePool
 - d3d11_2/ID3D11DeviceContext2::ResizeTilePool
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext2.ResizeTilePool
---

# ID3D11DeviceContext2::ResizeTilePool


## -description

Resizes a tile pool.

## -parameters

### -param pTilePool [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a> for the tile pool to resize.

### -param NewSizeInBytes [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

The new size in bytes of the tile pool. The size must be a multiple of 64 KB or 0.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the following:

<ul>
<li>Returns <b>E_INVALIDARG</b> if the new tile pool size isn't a multiple of 64 KB or 0.</li>
<li>Returns <b>E_OUTOFMEMORY</b> if the call results in the driver having to allocate space for new page table mappings but running out of memory.</li>
<li>Returns <b>DXGI_ERROR_DEVICE_REMOVED</b> if the video card has been physically removed from the system, or a driver upgrade for the video card has occurred.</li>
</ul>
For <b>E_INVALIDARG</b> or <b>E_OUTOFMEMORY</b>, the existing tile pool remains unchanged, which includes existing mappings.

## -remarks

<b>ResizeTilePool</b> increases or decreases the size of the tile pool depending on whether the app needs more or less working set for the tiled resources that are mapped into it. An app can allocate additional tile pools for new tiled resources, but if any single tiled resource needs more space than initially available in its tile pool, the app can increase the size of the resource's tile pool. A tiled resource can't have mappings into multiple tile pools simultaneously. 

When you increase the size of a tile pool, additional tiles are added to the end of the tile pool via one or more new allocations by the driver; your app can't detect the breakdown into the new allocations. Existing memory in the tile pool is left untouched, and existing tiled resource mappings into that memory remain intact.

When you decrease the size of a tile pool, tiles are removed from the end (this is allowed even below the initial allocation size, down to 0). This means that new mappings can't be made past the new size. But, existing mappings past the end of the new size remain intact and useable. The memory is kept active as long as mappings to any part of the allocations that are being used for the tile pool memory remains. If after decreasing, some memory has been kept active because tile mappings are pointing to it and the tile pool is increased again (by any amount), the existing memory is reused first before any additional allocations occur to service the size of the increase. 

To be able to save memory, an app has to not only decrease a tile pool but also remove and remap existing mappings past the end of the new smaller tile pool size.

The act of decreasing (and removing mappings) doesn't necessarily produce immediate memory savings. Freeing of memory depends on how granular the driver's underlying allocations for the tile pool are. When a decrease in the size of a tile pool happens to be enough to make a driver allocation unused, the driver can free the allocation. If a tile pool was increased and if you then decrease to previous sizes (and remove and remap tile mappings correspondingly), you will most likely yield memory savings. But, this scenario isn't guaranteed in the case that the sizes don't exactly align with the underlying allocation sizes chosen by the driver. 

For more info about tiled resources, see <a href="/windows/desktop/direct3d11/tiled-resources">Tiled resources</a>.

## -see-also

<a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2">ID3D11DeviceContext2</a>