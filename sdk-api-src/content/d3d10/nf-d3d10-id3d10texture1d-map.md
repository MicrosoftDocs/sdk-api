---
UID: NF:d3d10.ID3D10Texture1D.Map
title: ID3D10Texture1D::Map
author: windows-sdk-content
description: Get a pointer to the data contained in a subresource, and deny the GPU access to that subresource.
old-location: direct3d10\id3d10texture1d_map.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture1d_map.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 5214af3e-18cb-ccc4-745e-e8e5f90ef5cc, ID3D10Texture1D interface [Direct3D 10],Map method, ID3D10Texture1D.Map, ID3D10Texture1D::Map, Map, Map method [Direct3D 10], Map method [Direct3D 10],ID3D10Texture1D interface, d3d10/ID3D10Texture1D::Map, direct3d10.id3d10texture1d_map
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D10_USAGE
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Texture1D::Map


## -description


Get a pointer to the data contained in a subresource, and deny the GPU access to that subresource.


## -parameters




### -param Subresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index number of the subresource. See <a href="https://msdn.microsoft.com/48079797-b5c8-487b-a343-a5623b780350">D3D10CalcSubresource</a> for more details.


### -param MapType [in]

Type: <b><a href="https://msdn.microsoft.com/6a8e10cf-2cab-41f0-ba43-afa6854477ff">D3D10_MAP</a></b>

Specifies the CPU's read and write permissions for a resource. For possible values, see <a href="https://msdn.microsoft.com/6a8e10cf-2cab-41f0-ba43-afa6854477ff">D3D10_MAP</a>.


### -param MapFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


<a href="https://msdn.microsoft.com/cc8a1dae-4a48-4894-8ef4-67289062400d">Flag</a> that specifies what the CPU should do when the GPU is busy. This flag is optional.


### -param ppData [out]

Type: <b>void**</b>

Pointer to the texture resource data.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this function succeeds, it returns S_OK. For other restrictions, and a listing of error values that can be returned by any of the <b>Map</b> methods, see Remarks.




## -remarks



<h3><a id="Remarks"></a><a id="remarks"></a><a id="REMARKS"></a></h3>
Mapping a texture enables the CPU to directly access the underlying data in the subresource of a texture. For the method to succeed, the texture being mapped must be created with the appropriate flags (see <a href="https://msdn.microsoft.com/0f3dfe49-f4e0-4a66-a6f7-47170b0daa0b">D3D10_CPU_ACCESS_FLAG</a>), and its specified usage (see <a href="https://msdn.microsoft.com/eaaf695c-e99d-4bf8-b479-fa2d06d53248">D3D10_USAGE</a>) must be either D3D10_USAGE_DYNAMIC or D3D10_USAGE_STAGING.

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
 

For more information about the preceding return values, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.

<b>Map</b> has the following restrictions:

<ul>
<li>A single subresource cannot be mapped multiple times; in other words, do not call <b>Map</b> on a subresource that is already mapped.</li>
<li>Any subresource that is bound to the pipeline must be unmapped before any render operation (that is, before <a href="https://msdn.microsoft.com/01847bc8-3a58-4296-9e67-2fecd3832e48">ID3D10Device::Draw</a>) can be executed.</li>
</ul>
Applications must cast the void pData pointer to the appropriate type to meaningfully access the underlying subresource data. For example, the following code demonstrates how to read each texel of a 1D subresource. It is assumed that the texture was created using <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R32G32B32A32_FLOAT</a> and that pData is the pointer to the texture resource data output from a successful call to this method.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
FLOAT* pTexels = (FLOAT*)pData;
for( UINT col = 0; col &lt; width; col++ )
{
  pTexels[col*4 + 0]; // Alpha
  pTexels[col*4 + 1]; // Blue
  pTexels[col*4 + 2]; // Green
  pTexels[col*4 + 3]; // Red
}
</pre>
</td>
</tr>
</table></span></div>
<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

<b>Map</b> in Direct3D 10 is analogous to resource <a href="https://msdn.microsoft.com/b17d8262-e514-4b9c-9237-653a4258a14e">Lock</a> in Direct3D 9.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d73cdd85-d6e2-4724-a069-6a4edb5b354e">ID3D10Texture1D Interface</a>
 

 

