---
UID: NF:d3d10.ID3D10Buffer.Map
title: ID3D10Buffer::Map (d3d10.h)
description: Get a pointer to the data contained in the resource and deny GPU access to the resource.
helpviewer_keywords: ["7d41a2a2-1ba6-cc42-c30b-821d5734b5c3","ID3D10Buffer interface [Direct3D 10]","Map method","ID3D10Buffer.Map","ID3D10Buffer::Map","Map","Map method [Direct3D 10]","Map method [Direct3D 10]","ID3D10Buffer interface","d3d10/ID3D10Buffer::Map","direct3d10.id3d10buffer_map"]
old-location: direct3d10\id3d10buffer_map.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10buffer_map.htm
ms.date: 12/05/2018
ms.keywords: 7d41a2a2-1ba6-cc42-c30b-821d5734b5c3, ID3D10Buffer interface [Direct3D 10],Map method, ID3D10Buffer.Map, ID3D10Buffer::Map, Map, Map method [Direct3D 10], Map method [Direct3D 10],ID3D10Buffer interface, d3d10/ID3D10Buffer::Map, direct3d10.id3d10buffer_map
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Buffer::Map
 - d3d10/ID3D10Buffer::Map
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Buffer.Map
---

# ID3D10Buffer::Map


## -description

Get a pointer to the data contained in the resource and deny GPU access to the resource.

## -parameters

### -param MapType [in]

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_map">D3D10_MAP</a></b>

Flag that specifies the CPU's permissions for the reading and writing of a resource. For possible values, see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_map">D3D10_MAP</a>.

### -param MapFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flag that specifies what the CPU should do when the GPU is busy (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_map_flag">D3D10_MAP_FLAG</a>). This flag is optional.

### -param ppData [out]

Type: <b>void**</b>

Pointer to the buffer resource data.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this function succeeds, it returns S_OK. The following list contains some of the reasons that <b>Map</b> can fail:
      

<ul>
<li>If <i>MapFlags</i> specifies D3D10_MAP_FLAG_DO_NOT_WAIT and the GPU is not yet finished with the resource, <b>ID3D10Buffer::Map</b> 
        returns DXGI_ERROR_WAS_STILL_DRAWING.</li>
<li><b>ID3D10Buffer::Map</b> returns DXGI_ERROR_DEVICE_REMOVED if <i>MapType</i> includes any flags that permit reading and the hardware 
        device (that is, the video card) has been removed.</li>
</ul>
For more information about the preceding return values, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

For the CPU to write the contents of a resource, the resource must be created with the dynamic usage flag, D3D10_USAGE_DYNAMIC. 
      To both read and write those contents, the resource must be created with the staging usage flag, D3D10_USAGE_STAGING. (For more information about 
      these flags, see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">D3D10_USAGE</a>.) <b>ID3D10Buffer::Map</b> will retrieve a pointer to the resource data. 
      For a discussion on how to access resources efficiently, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping">Copying and Accessing Resource Data (Direct3D 10)</a>.

Call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10buffer-unmap">ID3D10Buffer::Unmap</a> to signify that the application has finished accessing the resource.

<b>ID3D10Buffer::Map</b> has a few other restrictions. For example:

<ul>
<li>The same buffer cannot be mapped multiple times; in other words, do not call <b>ID3D10Buffer::Map</b> on a buffer that is already mapped.</li>
<li>Any buffer that is bound to the pipeline must be unmapped before any rendering operation (that is, <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-draw">ID3D10Device::Draw</a>) 
        can be executed.</li>
</ul>
<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

<b>ID3D10Buffer::Map</b> in Direct3D 10 is analogous to resource <a href="/windows/desktop/direct3d9/locking-resources">Lock</a> in Direct3D 9.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer Interface</a>