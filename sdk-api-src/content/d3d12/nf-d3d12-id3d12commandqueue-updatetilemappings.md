---
UID: NF:d3d12.ID3D12CommandQueue.UpdateTileMappings
title: ID3D12CommandQueue::UpdateTileMappings (d3d12.h)
description: Updates mappings of tile locations in reserved resources to memory locations in a resource heap.
helpviewer_keywords: ["ID3D12CommandQueue interface","UpdateTileMappings method","ID3D12CommandQueue.UpdateTileMappings","ID3D12CommandQueue::UpdateTileMappings","UpdateTileMappings","UpdateTileMappings method","UpdateTileMappings method","ID3D12CommandQueue interface","d3d12/ID3D12CommandQueue::UpdateTileMappings","direct3d12.id3d12commandqueue_updatetilemappings"]
old-location: direct3d12\id3d12commandqueue_updatetilemappings.htm
tech.root: direct3d12
ms.assetid: 8A8017E5-AB55-4660-855B-D6F93F69CB52
ms.date: 12/05/2018
ms.keywords: ID3D12CommandQueue interface,UpdateTileMappings method, ID3D12CommandQueue.UpdateTileMappings, ID3D12CommandQueue::UpdateTileMappings, UpdateTileMappings, UpdateTileMappings method, UpdateTileMappings method,ID3D12CommandQueue interface, d3d12/ID3D12CommandQueue::UpdateTileMappings, direct3d12.id3d12commandqueue_updatetilemappings
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12CommandQueue::UpdateTileMappings
 - d3d12/ID3D12CommandQueue::UpdateTileMappings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12CommandQueue.UpdateTileMappings
---

# ID3D12CommandQueue::UpdateTileMappings


## -description

Updates mappings of tile locations in reserved resources to memory locations in a resource heap.

## -parameters

### -param pResource [in]

A pointer to the reserved resource.

### -param NumResourceRegions

The number of reserved resource regions.

### -param pResourceRegionStartCoordinates [in, optional]

An array of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate">D3D12_TILED_RESOURCE_COORDINATE</a> structures that describe the starting coordinates of the reserved resource regions. The <i>NumResourceRegions</i> parameter specifies the number of <b>D3D12_TILED_RESOURCE_COORDINATE</b> structures in the array.

### -param pResourceRegionSizes [in, optional]

An array of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size">D3D12_TILE_REGION_SIZE</a> structures that describe the sizes of the reserved resource regions. The <i>NumResourceRegions</i> parameter specifies the number of <b>D3D12_TILE_REGION_SIZE</b> structures in the array.

### -param pHeap [in, optional]

A pointer to the resource heap.

### -param NumRanges

The number of tile  ranges.

### -param pRangeFlags [in, optional]

A pointer to an  array of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_range_flags">D3D12_TILE_RANGE_FLAGS</a> values that describes each tile range. The <i>NumRanges</i> parameter specifies the number of values in the array.

### -param pHeapRangeStartOffsets [in, optional]

An array of offsets into the resource heap. These are 0-based tile offsets, counting in tiles (not bytes).

### -param pRangeTileCounts [in, optional]

An array of tiles.
            An array of values that specify the number of tiles in each tile range. The <i>NumRanges</i> parameter specifies the number of values in the array.

### -param Flags

A combination of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_mapping_flags">D3D12_TILE_MAPPING_FLAGS</a> values that are combined by using a bitwise OR operation.

## -remarks

Use <b>UpdateTileMappings</b> to map the virtual pages of a reserved resource to the physical pages of a heap. The mapping does not have to be in order. The operation is similar to  <a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings">ID3D11DeviceContext2::UpdateTileMappings</a> with the one key difference that D3D12 allows a reserved resource to have tiles from multiple heaps.

In a single call to <b>UpdateTileMappings</b>, you can map one or more ranges of resource tiles to one or more ranges of heap tiles. 
      

You can organize the parameters of  <b>UpdateTileMappings</b> in these ways to perform an update:
          

<ul>
<li><b>Reserved resource whose mappings are updated.</b> Mappings start off all NULL when a resource is initially created.
          </li>
<li><b>Set of tile regions on the reserved resource whose mappings are updated.</b> You can make one <b>UpdateTileMappings</b> call to update many mappings or multiple calls with a bit more API call overhead as well if that is more convenient. <ul>
<li><i>NumResourceRegions</i> specifies how many regions there are.</li>
<li><i>pResourceRegionStartCoordinates</i> and <i>pResourceRegionSizes</i> are each arrays that identify the start location and extend of each region. If <i>NumResourceRegions</i> is 1, for convenience either or both of the arrays that describe the regions can be NULL.  NULL for <i>pResourceRegionStartCoordinates</i> means the start coordinate is all 0s, and NULL for <i>pResourceRegionSizes</i> identifies a default region that is the full set of tiles for the entire reserved resource, including all mipmaps, array slices, or both.  </li>
<li>
If <i>pResourceRegionStartCoordinates</i> isn't NULL and <i>pResourceRegionSizes</i> is NULL, the region size defaults to 1 tile for all regions.  This makes it easy to define mappings for a set of individual tiles each at disparate locations by providing an array of locations in <i>pResourceRegionStartCoordinates</i> without having to send an array of <i>pResourceRegionSizes</i> all set to 1.
            

</li>
</ul>
The updates are applied from first region to last; so, if regions overlap in a single call, the updates later in the list overwrite the areas that overlap with previous updates.

</li>
<li><b>Heap that provides memory where tile mappings can go.</b>  If <b>UpdateTileMappings</b> only defines NULL mappings, you don't need to specify a heap.</li>
<li><b>Set of tile ranges where mappings are going.</b> Each given tile range can specify one of a few types of ranges: a range of tiles in a heap (default), a count of tiles in the reserved resource to map to a single tile in a heap (sharing the tile), a count of tile mappings in the reserved resource to skip and leave as they are, or a count of tiles in the heap to map to NULL.<i>NumRanges</i> specifies the number of tile ranges, where the total tiles identified across all ranges must match the total number of tiles in the tile regions from the previously described reserved resource.  Mappings are defined by iterating through the tiles in the tile regions in sequential order - x then y then z order for box regions - while walking through the set of tile ranges in sequential order.  The breakdown of tile regions doesn't have to line up with the breakdown of tile ranges, but the total number of tiles on both sides must be equal so that each reserved resource tile specified has a mapping specified.
            

<i>pRangeFlags</i>, <i>pHeapRangeStartOffsets</i>, and <i>pRangeTileCounts</i> are all arrays, of size <i>NumRanges</i>, that describe the tile ranges.  If <i>pRangeFlags</i> is NULL, all ranges are sequential tiles in the heap; otherwise, for each range i,<i>pRangeFlags[i]</i> identifies how the mappings in that range of tiles work:
              

<ul>
<li>If <i>pRangeFlags[i]</i> is <b>D3D12_TILE_RANGE_FLAG_NONE</b>, that range defines sequential tiles in the heap, with the number of tiles being <i>pRangeTileCounts[i]</i> and the starting location <i>pHeapRangeStartOffsets[i]</i>.  If <i>NumRanges</i> is 1, <i>pRangeTileCounts</i> can be NULL and defaults to the total number of tiles specified by all the tile regions.
              </li>
<li>If <i>pRangeFlags[i]</i> is <b>D3D12_TILE_RANGE_FLAG_REUSE_SINGLE_TILE</b>, <i>pHeapRangeStartOffsets[i]</i> identifies the single tile in the heap to map to, and <i>pRangeTileCounts[i]</i> specifies how many tiles from the tile regions to map to that heap location.  If <i>NumRanges</i> is 1, <i>pRangeTileCounts</i> can be NULL and defaults to the total number of tiles specified by all the tile regions.
              </li>
<li>If <i>pRangeFlags[i]</i> is <b>D3D12_TILE_RANGE_FLAG_NULL</b>, <i>pRangeTileCounts[i]</i> specifies how many tiles from the tile regions to map to NULL.  If <i>NumRanges</i> is 1, <i>pRangeTileCounts</i> can be NULL and defaults to the total number of tiles specified by all the tile regions. <i>pHeapRangeStartOffsets[i]</i> is ignored for NULL mappings.
              </li>
<li>If <i>pRangeFlags[i]</i> is <b>D3D12_TILE_RANGE_FLAG_SKIP</b>, <i>pRangeTileCounts[i]</i> specifies how many tiles from the tile regions to skip over and leave existing mappings unchanged for.  This can be useful if a tile region conveniently bounds an area of tile mappings to update except with some exceptions that need to be left the same as whatever they were mapped to before. <i>pHeapRangeStartOffsets[i]</i> is ignored for SKIP mappings.
              </li>
</ul>
</li>
</ul>
Reserved resources must follow the same rules for tile aliasing, initialization, and data inheritance as placed resources. See <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource">CreatePlacedResource</a> for more details.

Here are some examples of common <b>UpdateTileMappings</b> cases:
      


#### Examples

The examples reference the following structures and enums:

<ul>
<li>
<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate">D3D12_TILED_RESOURCE_COORDINATE</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size">D3D12_TILE_REGION_SIZE</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_range_flags">D3D12_TILE_RANGE_FLAGS</a>
</li>
</ul>
Clearing an entire surface's mappings to NULL


```cpp
// - NULL for pResourceRegionStartCoordinates and pResourceRegionSizes defaults to the entire resource
// - NULL for pHeapRangeStartOffsets since it isn't needed for mapping tiles to NULL
// - NULL for pRangeTileCounts when NumRanges is 1 defaults to the same number of tiles as the resource region (which is
//   the entire surface in this case)
//
UINT RangeFlags = D3D12_TILE_RANGE_FLAG_NULL;
pCommandQueue->UpdateTileMappings(pResource, 1, NULL, NULL, NULL, 1, &RangeFlags, NULL, NULL, D3D12_TILE_MAPPING_FLAG_NONE);

```


Mapping a region of tiles to a single tile:
        


```cpp
// - This maps a 2x3 tile region at tile offset (1,1) in a resource to tile [12] in a heap
// 
D3D12_TILED_RESOURCE_COORDINATE TRC;
TRC.X = 1;
TRC.Y = 1;
TRC.Z = 0;
TRC.Subresource = 0;

D3D12_TILE_REGION_SIZE TRS;
TRS.bUseBox = TRUE;
TRS.Width = 2;
TRS.Height = 3; 
TRS.Depth = 1;
TRS.NumTiles = TRS.Width * TRS.Height * TRS.Depth;

UINT RangeFlags = D3D12_TILE_RANGE_FLAG_REUSE_SINGLE_TILE;
UINT StartOffset = 12;

pCommandQueue->UpdateTileMappings(pResource,1,&TRC,&TRS,pHeap,1,&RangeFlags,&StartOffset,NULL,D3D12_TILE_MAPPING_FLAG_NONE);

```


Defining mappings for a set of disjoint individual tiles:
        


```cpp
// - This can also be accomplished in multiple calls. 
//   A single call to define multiple mapping updates can reduce CPU call overhead slightly,
//   at the cost of having to pass arrays as parameters.
// - Passing NULL for pResourceRegionSizes defaults to each region in the resource
//   being a single tile.  So all that is needed are the coordinates of each one.
// - Passing NULL for pRangeFlags defaults to no flags (since none are needed in this case)
// - Passing NULL for pRangeTileCounts defaults to each range in the heap being size 1.
//   So all that is needed are the start offsets for each tile in the heap
//
D3D12_TILED_RESOURCE_COORDINATE TRC[3];
UINT StartOffsets[3];
UINT NumSingleTiles = 3;
TRC[0].X = 1;
TRC[0].Y = 1; 
TRC[0].Subresource = 0;

StartOffsets[0] = 1;
TRC[1].X = 4;
TRC[1].Y = 7; 
TRC[1].Subresource = 0;
StartOffsets[1] = 4;

TRC[2].X = 2;
TRC[2].Y = 3; 
TRC[2].Subresource = 0;
StartOffsets[2] = 7;

pCommandQueue->UpdateTileMappings(pResource,NumSingleTiles,&TRC,NULL,pHeap,NumSingleTiles,NULL,StartOffsets,
NULL,D3D12_TILE_MAPPING_FLAG_NONE);

```


Complex example - defining mappings for regions with some skips, some NULL mappings. 


```cpp
// - This complex example hard codes the parameter arrays, whereas in practice the 
//   application would likely configure the parameters programatically or in a data driven way.
// - Suppose we have 3 regions in a resource to configure mappings for, 2x3 at coordinate (1,1),
//   3x3 at coordinate (4,7), and 7x1 at coordinate (20,30)
// - The tiles in the regions are walked from first to last, in X then Y then Z order,
//   while stepping forward through the specified Tile Ranges to determine each mapping.
//   In this example, 22 tile mappings need to be defined.
// - Suppose we want the first 3 tiles to be mapped to a contiguous range in the heap starting at
//   heap location [9], the next 8 to be skipped (left unchanged), the next 2 to map to NULL, 
//   the next 5 to share a single tile (heap location [17]) and the remaining 
//   4 tiles to each map to to unique heap locations, [2], [9], [4] and [17]:
//
D3D12_TILED_RESOURCE_COORDINATE TRC[3];
D3D12_TILE_REGION_SIZE TRS[3];
UINT NumRegions = 3;

TRC[0].X = 1;
TRC[0].Y = 1; 
TRC[0].Subresource = 0;
TRS[0].bUseBox = TRUE;
TRS[0].Width = 2;
TRS[0].Height = 3; 
TRS[0].NumTiles = TRS[0].Width * TRS[0].Height;

TRC[1].X = 4;
TRC[1].Y = 7; 
TRC[1].Subresource = 0;
TRS[1].bUseBox = TRUE;
TRS[1].Width = 3;
TRS[1].Height = 3; 
TRS[1].NumTiles = TRS[1].Width * TRS[1].Height;

TRC[2].X = 20;
TRC[2].Y = 30; 
TRC[2].Subresource = 0;
TRS[2].bUseBox = TRUE;
TRS[2].Width = 7;
TRS[2].Height = 1; 
TRS[2].NumTiles = TRS[2].Width * TRS[2].Height;

UINT NumRanges = 8;
UINT RangeFlags[8];
UINT HeapRangeStartOffsets[8];
UINT RangeTileCounts[8];

RangeFlags[0] = 0;
HeapRangeStartOffsets[0] = 9;
RangeTileCounts[0] = 3;

RangeFlags[1] = D3D12_TILE_RANGE_FLAG_SKIP;
HeapRangeStartOffsets[1] = 0; // offset is ignored for skip mappings
RangeTileCounts[1] = 8;

RangeFlags[2] = D3D12_TILE_RANGE_FLAG_NULL;
HeapRangeStartOffsets[2] = 0; // offset is ignored for NULL mappings
RangeTileCounts[2] = 2;

RangeFlags[3] = D3D12_TILE_RANGE_FLAG_REUSE_SINGLE_TILE;
HeapRangeStartOffsets[3] = 17; 
RangeTileCounts[3] = 5;

RangeFlags[4] = 0;
HeapRangeStartOffsets[4] = 2; 
RangeTileCounts[4] = 1;

RangeFlags[5] = 0;
HeapRangeStartOffsets[5] = 9; 
RangeTileCounts[5] = 1;

RangeFlags[6] = 0;
HeapRangeStartOffsets[6] = 4; 
RangeTileCounts[6] = 1;

RangeFlags[7] = 0;
HeapRangeStartOffsets[7] = 17; 
RangeTileCounts[7] = 1;

pCommandQueue->UpdateTileMappings(pResource,NumRegions,TRC,TRS,pHeap,NumRanges,RangeFlags,
HeapRangeStartOffsets,RangeTileCounts,D3D12_TILE_MAPPING_FLAG_NONE);

```

## -see-also

<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings">CopyTileMappings</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue">ID3D12CommandQueue</a>



<a href="/windows/desktop/direct3d12/volume-tiled-resources">Volume Tiled Resources</a>