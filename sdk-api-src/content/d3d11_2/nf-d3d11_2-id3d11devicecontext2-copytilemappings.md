---
UID: NF:d3d11_2.ID3D11DeviceContext2.CopyTileMappings
title: ID3D11DeviceContext2::CopyTileMappings
author: windows-sdk-content
description: Copies mappings from a source tiled resource to a destination tiled resource.
old-location: direct3d11\id3d11devicecontext2_copytilemappings.htm
tech.root: direct3d11
ms.assetid: 03EBF4F5-CEC3-485D-8124-AAB90DA4D6E1
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CopyTileMappings, CopyTileMappings method [Direct3D 11], CopyTileMappings method [Direct3D 11],ID3D11DeviceContext2 interface, ID3D11DeviceContext2 interface [Direct3D 11],CopyTileMappings method, ID3D11DeviceContext2.CopyTileMappings, ID3D11DeviceContext2::CopyTileMappings, d3d11_2/ID3D11DeviceContext2::CopyTileMappings, direct3d11.id3d11devicecontext2_copytilemappings
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext2.CopyTileMappings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext2::CopyTileMappings


## -description


Copies mappings from a source tiled resource to a destination tiled resource.


## -parameters




### -param pDestTiledResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

A pointer to the destination tiled resource.


### -param pDestRegionStartCoordinate [in]

Type: <b>const <a href="https://msdn.microsoft.com/4639E5FA-44D7-4F6E-8843-17EE862BD9C4">D3D11_TILED_RESOURCE_COORDINATE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/4639E5FA-44D7-4F6E-8843-17EE862BD9C4">D3D11_TILED_RESOURCE_COORDINATE</a> structure that describes the starting coordinates of the destination tiled resource.
       


### -param pSourceTiledResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

A pointer to the source tiled resource.


### -param pSourceRegionStartCoordinate [in]

Type: <b>const <a href="https://msdn.microsoft.com/4639E5FA-44D7-4F6E-8843-17EE862BD9C4">D3D11_TILED_RESOURCE_COORDINATE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/4639E5FA-44D7-4F6E-8843-17EE862BD9C4">D3D11_TILED_RESOURCE_COORDINATE</a> structure that describes the starting coordinates of the source tiled resource.
       


### -param pTileRegionSize [in]

Type: <b>const <a href="https://msdn.microsoft.com/D4A93462-9A2F-416A-9CC1-AC24DFF35890">D3D11_TILE_REGION_SIZE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/D4A93462-9A2F-416A-9CC1-AC24DFF35890">D3D11_TILE_REGION_SIZE</a> structure that describes the size of the tiled region.
       


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/13B4665C-F8A2-45A7-BBE9-FEB45FB08963">D3D11_TILE_MAPPING_FLAGS</a> values that are combined by using a bitwise OR operation. The only valid value is <b>D3D11_TILE_MAPPING_NO_OVERWRITE</b>, which indicates that previously submitted commands to the device that may still be executing do not reference any of the tile region being updated. The device can then avoid having to flush previously submitted work to perform the tile mapping update.  If the app violates this promise by updating tile mappings for locations in tiled resources that are still being referenced by outstanding commands, undefined rendering behavior results, including the potential for significant slowdowns on some architectures.  This is like the "no overwrite" concept that exists elsewhere in the Direct3D API, except applied to the tile mapping data structure itself (which in hardware is a page table). The absence of the <b>D3D11_TILE_MAPPING_NO_OVERWRITE</b> value requires that tile mapping updates that <b>CopyTileMappings</b> specifies must be completed before any subsequent Direct3D command can proceed.
       


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the following:
         

<ul>
<li>Returns <b>E_INVALIDARG</b> if various conditions such as invalid flags or passing in non Tiled Resources result in the call being dropped.
             The dest and the source regions must each entirely fit in their resource or behavior is undefined (debug layer will emit an error).
             

</li>
<li>Returns <b>E_OUTOFMEMORY</b> if the call results in the driver having to allocate space for new page table mappings but running out of memory.
             If out of memory occurs when this is called in a commandlist and the commandlist is being executed, the device will be removed. Applications can avoid this situation by only doing update calls that change existing mappings from Tiled Resources within commandlists (so drivers will not have to allocate page table memory, only change the mapping).
             

</li>
</ul>



## -remarks



<b>CopyTileMappings</b> helps with tasks such as shifting mappings around within and across tiled resources, for example, scrolling tiles. The source and destination regions can overlap; the result of the copy in this situation is as if the source was saved to a temp location and then from there written to the destination.

For more info about tiled resources, see <a href="https://msdn.microsoft.com/03083460-192B-40CB-8EE1-76DF6D95F72B">Tiled resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a>
 

 

