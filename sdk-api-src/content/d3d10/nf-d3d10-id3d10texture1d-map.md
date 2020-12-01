---
UID: NF:d3d10.ID3D10Texture1D.Map
title: ID3D10Texture1D::Map (d3d10.h)
description: Get a pointer to the data contained in a subresource, and deny the GPU access to that subresource.
helpviewer_keywords: ["5214af3e-18cb-ccc4-745e-e8e5f90ef5cc","ID3D10Texture1D interface [Direct3D 10]","Map method","ID3D10Texture1D.Map","ID3D10Texture1D::Map","Map","Map method [Direct3D 10]","Map method [Direct3D 10]","ID3D10Texture1D interface","d3d10/ID3D10Texture1D::Map","direct3d10.id3d10texture1d_map"]
old-location: direct3d10\id3d10texture1d_map.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture1d_map.htm
ms.date: 12/05/2018
ms.keywords: 5214af3e-18cb-ccc4-745e-e8e5f90ef5cc, ID3D10Texture1D interface [Direct3D 10],Map method, ID3D10Texture1D.Map, ID3D10Texture1D::Map, Map, Map method [Direct3D 10], Map method [Direct3D 10],ID3D10Texture1D interface, d3d10/ID3D10Texture1D::Map, direct3d10.id3d10texture1d_map
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
 - ID3D10Texture1D::Map
 - d3d10/ID3D10Texture1D::Map
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
 - ID3D10Texture1D.Map
---

# ID3D10Texture1D::Map


## -description

Get a pointer to the data contained in a subresource, and deny the GPU access to that subresource.

## -parameters

### -param Subresource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index number of the subresource. See <a href="/windows/desktop/api/d3d10/nf-d3d10-d3d10calcsubresource">D3D10CalcSubresource</a> for more details.

### -param MapType [in]

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_map">D3D10_MAP</a></b>

Specifies the CPU's read and write permissions for a resource. For possible values, see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_map">D3D10_MAP</a>.

### -param MapFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_map_flag">Flag</a> that specifies what the CPU should do when the GPU is busy. This flag is optional.

### -param ppData [out]

Type: <b>void**</b>

Pointer to the texture resource data.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this function succeeds, it returns S_OK. For other restrictions, and a listing of error values that can be returned by any of the <b>Map</b> methods, see Remarks.

## -remarks

<h3><a id="Remarks"></a><a id="remarks"></a><a id="REMARKS"></a></h3>
Mapping a texture enables the CPU to directly access the underlying data in the subresource of a texture. For the method to succeed, the texture being mapped must be created with the appropriate flags (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_cpu_access_flag">D3D10_CPU_ACCESS_FLAG</a>), and its specified usage (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">D3D10_USAGE</a>) must be either D3D10_USAGE_DYNAMIC or D3D10_USAGE_STAGING.

Common failures of <b>Map</b> methods are indicated by the following return values:



<table>
<tr>
<th>Item</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="DXGI_ERROR_WAS_STILL_DRAWING"></a><a id="dxgi_error_was_still_drawing"></a>DXGI_ERROR_WAS_STILL_DRAWING

</td>
<td width="60%">
If <i>MapFlags</i> specifies D3D10_MAP_FLAG_DO_NOT_WAIT and the GPU is not yet finished with the resource, <b>Map</b> returns DXGI_ERROR_WAS_STILL_DRAWING.

</td>
</tr>
<tr>
<td width="40%">
<a id="DXGI_ERROR_DEVICE_REMOVED"></a><a id="dxgi_error_device_removed"></a>DXGI_ERROR_DEVICE_REMOVED

</td>
<td width="60%">
<b>Map</b> returns DXGI_ERROR_DEVICE_REMOVED if <i>MapType</i> allows any CPU read access and the video card has been removed.

</td>
</tr>
</table>
 

For more information about the preceding return values, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

<b>Map</b> has the following restrictions:

<ul>
<li>A single subresource cannot be mapped multiple times; in other words, do not call <b>Map</b> on a subresource that is already mapped.</li>
<li>Any subresource that is bound to the pipeline must be unmapped before any render operation (that is, before <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-draw">ID3D10Device::Draw</a>) can be executed.</li>
</ul>
Applications must cast the void pData pointer to the appropriate type to meaningfully access the underlying subresource data. For example, the following code demonstrates how to read each texel of a 1D subresource. It is assumed that the texture was created using <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_R32G32B32A32_FLOAT</a> and that pData is the pointer to the texture resource data output from a successful call to this method.


```

FLOAT* pTexels = (FLOAT*)pData;
for( UINT col = 0; col < width; col++ )
{
  pTexels[col*4 + 0]; // Alpha
  pTexels[col*4 + 1]; // Blue
  pTexels[col*4 + 2]; // Green
  pTexels[col*4 + 3]; // Red
}

```


<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

<b>Map</b> in Direct3D 10 is analogous to resource <a href="/windows/desktop/direct3d9/locking-resources">Lock</a> in Direct3D 9.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10texture1d">ID3D10Texture1D Interface</a>