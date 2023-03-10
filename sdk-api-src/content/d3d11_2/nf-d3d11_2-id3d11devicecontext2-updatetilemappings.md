---
UID: NF:d3d11_2.ID3D11DeviceContext2.UpdateTileMappings
title: ID3D11DeviceContext2::UpdateTileMappings (d3d11_2.h)
description: Updates mappings of tile locations in tiled resources to memory locations in a tile pool.
helpviewer_keywords: ["ID3D11DeviceContext2 interface [Direct3D 11]","UpdateTileMappings method","ID3D11DeviceContext2.UpdateTileMappings","ID3D11DeviceContext2::UpdateTileMappings","UpdateTileMappings","UpdateTileMappings method [Direct3D 11]","UpdateTileMappings method [Direct3D 11]","ID3D11DeviceContext2 interface","d3d11_2/ID3D11DeviceContext2::UpdateTileMappings","direct3d11.id3d11devicecontext2_updatetilemappings"]
old-location: direct3d11\id3d11devicecontext2_updatetilemappings.htm
tech.root: direct3d11
ms.assetid: 542735C4-BFDE-4EA9-9595-BA30BD06422B
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext2 interface [Direct3D 11],UpdateTileMappings method, ID3D11DeviceContext2.UpdateTileMappings, ID3D11DeviceContext2::UpdateTileMappings, UpdateTileMappings, UpdateTileMappings method [Direct3D 11], UpdateTileMappings method [Direct3D 11],ID3D11DeviceContext2 interface, d3d11_2/ID3D11DeviceContext2::UpdateTileMappings, direct3d11.id3d11devicecontext2_updatetilemappings
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
 - ID3D11DeviceContext2::UpdateTileMappings
 - d3d11_2/ID3D11DeviceContext2::UpdateTileMappings
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
 - ID3D11DeviceContext2.UpdateTileMappings
---

# ID3D11DeviceContext2::UpdateTileMappings


## -description

Updates mappings of tile locations in tiled resources to memory locations in a tile pool.

## -parameters

### -param pTiledResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

A pointer to the tiled resource.

### -param NumTiledResourceRegions [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of tiled resource regions.

### -param pTiledResourceRegionStartCoordinates [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate">D3D11_TILED_RESOURCE_COORDINATE</a>*</b>

An array of <a href="/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate">D3D11_TILED_RESOURCE_COORDINATE</a> structures that describe the starting coordinates of the tiled resource regions. The <i>NumTiledResourceRegions</i> parameter specifies the number of <b>D3D11_TILED_RESOURCE_COORDINATE</b> structures in the array.

### -param pTiledResourceRegionSizes [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_tile_region_size">D3D11_TILE_REGION_SIZE</a>*</b>

An array of <a href="/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_tile_region_size">D3D11_TILE_REGION_SIZE</a> structures that describe the sizes of the tiled resource regions. The <i>NumTiledResourceRegions</i> parameter specifies the number of <b>D3D11_TILE_REGION_SIZE</b> structures in the array.

### -param pTilePool [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>*</b>

A pointer to the tile pool.

### -param NumRanges [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of tile-pool ranges.

### -param pRangeFlags [in, optional]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

An array of <a href="/windows/desktop/api/d3d11_2/ne-d3d11_2-d3d11_tile_range_flag">D3D11_TILE_RANGE_FLAG</a> values that describe each tile-pool range. The <i>NumRanges</i> parameter specifies the number of values in the array.

### -param pTilePoolStartOffsets [in, optional]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

An array of offsets into the tile pool. These are 0-based tile offsets, counting in tiles (not bytes).

### -param pRangeTileCounts [in, optional]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

An array of tiles. 

An array of values that specify the number of tiles in each tile-pool range. The <i>NumRanges</i> parameter specifies the number of values in the array.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A combination of <a href="/windows/desktop/api/d3d11_2/ne-d3d11_2-d3d11_tile_mapping_flag">D3D11_TILE_MAPPING_FLAGS</a> values that are combined by using a bitwise OR operation.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the following:

<ul>
<li>Returns <b>E_INVALIDARG</b> if various conditions such as invalid flags result in the call being dropped.The debug layer will emit an error.

</li>
<li>Returns <b>E_OUTOFMEMORY</b> if the call results in the driver having to allocate space for new page table mappings but running out of memory.If out of memory occurs when this is called in a commandlist and the commandlist is being executed, the device will be removed. Apps can avoid this situation by only doing update calls that change existing mappings from tiled resources within commandlists (so drivers will not have to allocate page table memory, only change the mapping).

</li>
<li>Returns <b>DXGI_ERROR_DEVICE_REMOVED</b> if the video card has been physically removed from the system, or a driver upgrade for the video card has occurred.
            </li>
</ul>

## -remarks

In a single call to <b>UpdateTileMappings</b>, you can map one or more ranges of resource tiles to one or more ranges of tile-pool tiles. 

You can organize the parameters of  <b>UpdateTileMappings</b> in these ways to perform an update:

<ul>
<li><b>Tiled resource whose mappings are updated.</b> This is a resource that was created with the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_TILED</a> flag. Mappings start off all NULL when a resource is initially created.</li>
<li><b>Set of tile regions on the tiled resource whose mappings are updated.</b> You can make one <b>UpdateTileMappings</b> call to update many mappings or multiple calls with a bit more API call overhead as well if that is more convenient. <i>NumTiledResourceRegions</i> specifies how many regions there are, <i>pTiledResourceRegionStartCoordinates</i> and <i>pTiledResourceRegionSizes</i> are each arrays that identify the start location and extend of each region. If <i>NumTiledResourceRegions</i> is 1, for convenience either or both of the arrays that describe the regions can be NULL.  NULL for <i>pTiledResourceRegionStartCoordinates</i> means the start coordinate is all 0s, and NULL for <i>pTiledResourceRegionSizes</i> identifies a default region that is the full set of tiles for the entire tiled resource, including all mipmaps, array slices, or both.  If <i>pTiledResourceRegionStartCoordinates</i> isn't NULL and <i>pTiledResourceRegionSizes</i> is NULL, the region size defaults to 1 tile for all regions.  This makes it easy to define mappings for a set of individual tiles each at disparate locations by providing an array of locations in <i>pTiledResourceRegionStartCoordinates</i> without having to send an array of <i>pTiledResourceRegionSizes</i> all set to 1.

The updates are applied from first region to last; so, if regions overlap in a single call, the updates later in the list overwrite the areas that overlap with previous updates.

</li>
<li><b>Tile pool that provides memory where tile mappings can go.</b> A tiled resource can point to a single tile pool at a time.  If a new tile pool is specified (for the first time or different from the last time a tile pool was specified), all existing tile mappings for the tiled resource are cleared and the new set of mappings in the current <b>UpdateTileMappings</b> call are applied for the new tile pool. If no tile pool is specified (NULL) or the same tile pool as a previous <b>UpdateTileMappings</b> call is provided, the <b>UpdateTileMappings</b> call just adds the new mappings to existing ones (overwriting on overlap). If <b>UpdateTileMappings</b> only defines NULL mappings, you don't need to specify a tile pool because it is irrelevant. But if you specify a tile pool anyway, it takes the same behavior as previously described when providing a tile pool. </li>
<li><b>Set of tile ranges where mappings are going.</b> Each given tile range can specify one of a few types of ranges: a range of tiles in a tile pool (default), a count of tiles in the tiled resource to map to a single tile in a tile pool (sharing the tile), a count of tile mappings in the tiled resource to skip and leave as they are, or a count of tiles in the tile pool to map to NULL.<i>NumRanges</i> specifies the number of tile ranges, where the total tiles identified across all ranges must match the total number of tiles in the tile regions from the previously described tiled resource.  Mappings are defined by iterating through the tiles in the tile regions in sequential order - x then y then z order for box regions - while walking through the set of tile ranges in sequential order.  The breakdown of tile regions doesn't have to line up with the breakdown of tile ranges, but the total number of tiles on both sides must be equal so that each tiled resource tile specified has a mapping specified.

<i>pRangeFlags</i>, <i>pTilePoolStartOffsets</i>, and <i>pRangeTileCounts</i> are all arrays, of size <i>NumRanges</i>, that describe the tile ranges.  If <i>pRangeFlags</i> is NULL, all ranges are sequential tiles in the tile pool; otherwise, for each range i, pRangeFlags[i] identifies how the mappings in that range of tiles work:

<ul>
<li>If pRangeFlags[i] is 0, that range defines sequential tiles in the tile pool, with the number of tiles being pRangeTileCounts[i] and the starting location pTilePoolStartOffsets[i].  If <i>NumRanges</i> is 1, <i>pRangeTileCounts</i> can be NULL and defaults to the total number of tiles specified by all the tile regions.</li>
<li>If pRangeFlags[i] is <b>D3D11_TILE_RANGE_REUSE_SINGLE_TILE</b>, pTilePoolStartOffsets[i] identifies the single tile in the tile pool to map to, and pRangeTileCounts[i] specifies how many tiles from the tile regions to map to that tile pool location.  If <i>NumRanges</i> is 1, <i>pRangeTileCounts</i> can be NULL and defaults to the total number of tiles specified by all the tile regions.</li>
<li>If pRangeFlags[i] is <b>D3D11_TILE_RANGE_NULL</b>, pRangeTileCounts[i] specifies how many tiles from the tile regions to map to NULL.  If <i>NumRanges</i> is 1, <i>pRangeTileCounts</i> can be NULL and defaults to the total number of tiles specified by all the tile regions. pTilePoolStartOffsets[i] is ignored for NULL mappings. </li>
<li>If pRangeFlags[i] is <b>D3D11_TILE_RANGE_SKIP</b>, pRangeTileCounts[i] specifies how many tiles from the tile regions to skip over and leave existing mappings unchanged for.  This can be useful if a tile region conveniently bounds an area of tile mappings to update except with some exceptions that need to be left the same as whatever they were mapped to before. pTilePoolStartOffsets[i] is ignored for SKIP mappings.</li>
</ul>
</li>
<li><b>Flags parameter for overall options.</b> <b>D3D11_TILE_MAPPING_NO_OVERWRITE</b> means the caller promises that previously submitted commands to the device that may still be executing do not reference any of the tile region being updated. This allows the device to avoid having to flush previously submitted work in order to do the tile mapping  update.  If the app violates this promise by updating tile mappings for locations in tiled resources still being referenced by outstanding commands, undefined rendering behavior results, which includes the potential for significant slowdowns on some architectures.  This is like the "no overwrite" concept that exists elsewhere in the Direct3D API, except applied to tile mapping data structure itself, which in hardware is a page table. The absence of this flag requires that tile mapping updates specified by this <b>UpdateTileMappings</b> call must be completed before any subsequent Direct3D command can proceed.</li>
</ul>
If tile mappings have changed on a tiled resource that the app will render via <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rendertargetview">RenderTargetView</a> or <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview">DepthStencilView</a>, the app must clear, by using the fixed function <b>Clear</b> APIs, the tiles that have changed within the area being rendered (mapped or not). If an app doesn't clear in these situations, the app receives undefined values when it reads from the tiled resource.  


<div class="alert"><b>Note</b>  In Direct3D 11.2, hardware can now support <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-clearview">ClearView</a> on depth-only formats. For more info, see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options1">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a>.</div>
<div> </div>
If an app needs to preserve existing memory contents of areas in a tiled resource where mappings have changed, the app can first save the contents where tile mappings have changed, by copying them to a temporary surface, for example using <a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-copytiles">CopyTiles</a>, issuing the required <b>Clear</b>, and then copying the contents back.


Suppose a tile is mapped into multiple tiled resources at the same time and tile contents are manipulated by any means (render, copy, and so on) via one of the tiled resources. Then, if the same tile is to be rendered via any other tiled resource, the tile must be cleared first as previously described.


For more info about tiled resources, see <a href="/windows/desktop/direct3d11/tiled-resources">Tiled resources</a>.

Here are some examples of common <b>UpdateTileMappings</b> cases:


#### Examples

Clearing an entire surface's mappings to NULL:


```cpp
// - No-overwrite is specified, assuming it is known nothing else the GPU could be doing is referencing the previous mappings
// - NULL for pTiledResourceRegionStatCoordinates and pTiledResourceRegionSizes defaults to the entire resource
// - NULL for pTilePoolStartOffsets since it isn't needed for mapping tiles to NULL
// - NULL for pRangeTileCounts when NumRanges is 1 defaults to the same number of tiles as the tiled resource region (which is
//   the entire surface in this case)
//
// UINT RangeFlags = D3D11_TILE_MAPPING_NULL;
// pDeviceContext2->UpdateTileMappings(pTiledResource,1,NULL,NULL,NULL,1,&RangeFlags,NULL,NULL,D3D11_TILE_MAPPING_NO_OVERWRITE);

```


Mapping a region of tiles to a single tile:


```cpp
// - This maps a 2x3 tile region at tile offset (1,1) in a Tiled Resource to tile [12] in a Tile Pool
// 
// D3D11_TILED_RESOURCE_COORDINATE TRC;
// TRC.X = 1;
// TRC.Y = 1;
// TRC.Z = 0;
// TRC.Subresource = 0;
//
// D3D11_TILE_REGION_SIZE TRS;
// TRS.bUseBox = TRUE;
// TRS.Width = 2;
// TRS.Height = 3; 
// TRS.Depth = 1;
// TRS.NumTiles = TRS.Width * TRS.Height * TRS.Depth;
// 
// UINT RangeFlags = D3D11_TILE_MAPPING_REUSE_SINGLE_TILE;
// UINT StartOffset = 12;
// pDeviceContext2->UpdateTileMappings(pTiledResource,1,&TRC,&TRS,pTilePool,1,&RangeFlags,&StartOffset,
//                                     NULL,D3D11_TILE_MAPPING_NO_OVERWRITE);

```


Defining mappings for a set of disjoint individual tiles:


```cpp
// - This can also be accomplished in multiple calls.  Using a single call to define multiple
//   a single call to define multiple mapping updates can reduce CPU call overhead slightly,
//   at the cost of having to pass arrays as parameters.
// - Passing NULL for pTiledResourceRegionSizes defaults to each region in the Tiled Resource
//   being a single tile.  So all that is needed are the coordinates of each one.
// - Passing NULL for Range Flags defaults to no flags (since none are needed in this case)
// - Passing NULL for pRangeTileCounts defaults to each range in the Tile Pool being size 1.
//   So all that is needed are the start offsets for each tile in the Tile Pool
//
// D3D11_TILED_RESOURCE_COORDINATE TRC[3];
// UINT StartOffsets[3];
// UINT NumSingleTiles = 3;
//
// TRC[0].X = 1;
// TRC[0].Y = 1; 
// TRC[0].Subresource = 0;
// StartOffsets[0] = 1;
//
// TRC[1].X = 4;
// TRC[1].Y = 7; 
// TRC[1].Subresource = 0;
// StartOffsets[1] = 4;
//
// TRC[2].X = 2;
// TRC[2].Y = 3; 
// TRC[2].Subresource = 0;
// StartOffsets[2] = 7;
//
// pDeviceContext2->UpdateTileMappings(pTiledResource,NumSingleTiles,&TRC,NULL,pTilePool,NumSingleTiles,NULL,StartOffsets,
//                                     NULL,D3D11_TILE_MAPPING_NO_OVERWRITE);

```


Complex example - defining mappings for regions with some skips, some NULL mappings:


```cpp
// - This complex example hard codes the parameter arrays, whereas in practice the 
//   application would likely configure the parameters programatically or in a data driven way.
// - Suppose we have 3 regions in a Tiled Resource to configure mappings for, 2x3 at coordinate (1,1),
//   3x3 at coordinate (4,7), and 7x1 at coordinate (20,30)
// - The tiles in the regions are walked from first to last, in X then Y then Z order,
//   while stepping forward through the specified Tile Ranges to determine each mapping.
//   In this example, 22 tile mappings need to be defined.
// - Suppose we want the first 3 tiles to be mapped to a contiguous range in the Tile Pool starting at
//   tile pool location [9], the next 8 to be skipped (left unchanged), the next 2 to map to NULL, 
//   the next 5 to share a single tile (tile pool location [17]) and the remaining 
//   4 tiles to each map to to unique tile pool locations, [2], [9], [4] and [17]:
//
// D3D11_TILED_RESOURCE_COORDINATE TRC[3];
// D3D11_TILE_REGION_SIZE TRS[3];
// UINT NumRegions = 3;
// 
// TRC[0].X = 1;
// TRC[0].Y = 1; 
// TRC[0].Subresource = 0;
// TRS[0].bUseBox = TRUE;
// TRS[0].Width = 2;
// TRS[0].Height = 3; 
// TRS[0].NumTiles = TRS[0].Width * TRS[0].Height;
//
// TRC[1].X = 4;
// TRC[1].Y = 7; 
// TRC[1].Subresource = 0;
// TRS[1].bUseBox = TRUE;
// TRS[1].Width = 3;
// TRS[1].Height = 3; 
// TRS[1].NumTiles = TRS[1].Width * TRS[1].Height;
//
// TRC[2].X = 20;
// TRC[2].Y = 30; 
// TRC[2].Subresource = 0;
// TRS[2].bUseBox = TRUE;
// TRS[2].Width = 7;
// TRS[2].Height = 1; 
// TRS[2].NumTiles = TRS[2].Width * TRS[2].Height;
//
// UINT NumRanges = 8;
// UINT RangeFlags[8];
// UINT TilePoolStartOffsets[8];
// UINT RangeTileCounts[8];
//
// RangeFlags[0] = 0;
// TilePoolStartOffsets[0] = 9;
// RangeTileCounts[0] = 3;
//
// RangeFlags[1] = D3D11_TILE_MAPPING_SKIP;
// TilePoolStartOffsets[1] = 0; // offset is ignored for skip mappings
// RangeTileCounts[1] = 8;
//
// RangeFlags[2] = D3D11_TILE_MAPPING_NULL;
// TilePoolStartOffsets[2] = 0; // offset is ignored for NULL mappings
// RangeTileCounts[2] = 2;
//
// RangeFlags[3] = D3D11_TILE_MAPPING_REUSE_SINGLE_TILE;
// TilePoolStartOffsets[3] = 17; 
// RangeTileCounts[3] = 5;
//
// RangeFlags[4] = 0;
// TilePoolStartOffsets[4] = 2; 
// RangeTileCounts[4] = 1;
//
// RangeFlags[5] = 0;
// TilePoolStartOffsets[5] = 9; 
// RangeTileCounts[5] = 1;
//
// RangeFlags[6] = 0;
// TilePoolStartOffsets[6] = 4; 
// RangeTileCounts[6] = 1;
//
// RangeFlags[7] = 0;
// TilePoolStartOffsets[7] = 17; 
// RangeTileCounts[7] = 1;
//
// pDeviceContext2->UpdateTileMappings(pTiledResource,NumRegions,TRC,TRS,pTilePool,NumRanges,RangeFlags,
//                                     TilePoolStartOffsets,RangeTileCounts,D3D11_TILE_MAPPING_NO_OVERWRITE);

```


CopyTileMappings


```cpp
// CopyTileMappings helps with tasks such as shifting mappings around within/across Tiled Resources, e.g. scrolling tiles.
// The source and dest region can overlap - the result of the copy in this case is as if the source was saved to a temp and then
// from there written to the dest, though the implementation may be able to do better. 
//
// The Flags field allows D3D11_TILE_MAPPING_NO_OVERWRITE to be specified, means the caller promises that previously 
//      submitted commands to the device that may still be executing do not reference any of the tile region being updated.
//      This allows the device to avoid having to flush previously submitted work in order to do the tile mapping 
//      update.  If the application violates this promise by updating tile mappings for locations in Tiled Resouces 
//      still being referenced by outstanding commands, undefined rendering behavior results, including the potential 
//      for significant slowdowns on some architectures.  This is like the "no overwrite" concept that exists 
//      elsewhere in the API, except applied to Tile Mapping data structure itself (which in hardware is a page table).
//      The absence of this flag requires that tile mapping updates specified by this call must be completed before any
//      subsequent D3D command can proceed.
//
// Return Values:
//
// Returns S_OK or E_INVALIDARG or E_OUTOFMEMORY.  The latter can happen if the call results in the driver having to 
// allocate space for new page table mappings but running out of memory.
//
// If out of memory occurs when this is called in a commandlist and the commandlist is being executed, the device will be removed.
// Applications can avoid this situation by only doing update calls that change existing mappings from Tiled Resources 
// within commandlists (so drivers will not have to allocate page table memory, only change the mapping).
//
// Various other basic conditions such as invalid flags or passing in non Tiled Resources result in call being dropped 
// with E_INVALIDARG.
// 
// Validation remarks:
//
// The dest and the source regions must each entirely fit in their resource or behavior is undefined 
// (debug layer will emit an error).

```

## -see-also

<a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2">ID3D11DeviceContext2</a>