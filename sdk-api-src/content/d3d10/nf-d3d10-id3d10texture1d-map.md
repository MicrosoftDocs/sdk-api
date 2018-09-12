---
UID: NF:d3d10.ID3D10Texture1D.Map
title: ID3D10Texture1D::Map
author: windows-sdk-content
description: Get a pointer to the data contained in a subresource, and deny the GPU access to that subresource.
old-location: direct3d10\id3d10texture1d_map.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture1d_map.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 5214af3e-18cb-ccc4-745e-e8e5f90ef5cc, ID3D10Texture1D interface [Direct3D 10],Map method, ID3D10Texture1D.Map, ID3D10Texture1D::Map, Map, Map method [Direct3D 10], Map method [Direct3D 10],ID3D10Texture1D interface, d3d10/ID3D10Texture1D::Map, direct3d10.id3d10texture1d_map
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Texture1D::Map


## -description


Get a pointer to the data contained in a subresource, and deny the GPU access to that subresource.


## -parameters




### -param Subresource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Index number of the subresource. See <a href="https://msdn.microsoft.com/en-us/library/Bb694525(v=VS.85).aspx">D3D10CalcSubresource</a> for more details.


### -param MapType [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205318(v=VS.85).aspx">D3D10_MAP</a></b>

Specifies the CPU's read and write permissions for a resource. For possible values, see <a href="https://msdn.microsoft.com/en-us/library/Bb205318(v=VS.85).aspx">D3D10_MAP</a>.


### -param MapFlags [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb205321(v=VS.85).aspx">Flag</a> that specifies what the CPU should do when the GPU is busy. This flag is optional.


### -param ppData [out]

Type: <b>void**</b>

Pointer to the texture resource data.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this function succeeds, it returns S_OK. For other restrictions, and a listing of error values that can be returned by any of the <b>Map</b> methods, see Remarks.




## -remarks



<h3><a id="Remarks"></a><a id="remarks"></a><a id="REMARKS"></a></h3>
Mapping a texture enables the CPU to directly access the underlying data in the subresource of a texture. For the method to succeed, the texture being mapped must be created with the appropriate flags (see <a href="https://msdn.microsoft.com/en-us/library/Bb204908(v=VS.85).aspx">D3D10_CPU_ACCESS_FLAG</a>), and its specified usage (see <a href="https://msdn.microsoft.com/en-us/library/Bb172499(v=VS.85).aspx">D3D10_USAGE</a>) must be either D3D10_USAGE_DYNAMIC or D3D10_USAGE_STAGING.

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
 

For more information about the preceding return values, see <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.

<b>Map</b> has the following restrictions:

<ul>
<li>A single subresource cannot be mapped multiple times; in other words, do not call <b>Map</b> on a subresource that is already mapped.</li>
<li>Any subresource that is bound to the pipeline must be unmapped before any render operation (that is, before <a href="https://msdn.microsoft.com/en-us/library/Bb173563(v=VS.85).aspx">ID3D10Device::Draw</a>) can be executed.</li>
</ul>
Applications must cast the void pData pointer to the appropriate type to meaningfully access the underlying subresource data. For example, the following code demonstrates how to read each texel of a 1D subresource. It is assumed that the texture was created using <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT_R32G32B32A32_FLOAT</a> and that pData is the pointer to the texture resource data output from a successful call to this method.


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

<b>Map</b> in Direct3D 10 is analogous to resource <a href="https://msdn.microsoft.com/en-us/library/Bb174707(v=VS.85).aspx">Lock</a> in Direct3D 9.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173863(v=VS.85).aspx">ID3D10Texture1D Interface</a>
 

 

