---
UID: NS:d3d10.D3D10_MAPPED_TEXTURE2D
title: D3D10_MAPPED_TEXTURE2D
author: windows-sdk-content
description: Provides access to subresource data in a 2D texture.
old-location: direct3d10\d3d10_mapped_texture2d.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_mapped_texture2d.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: D3D10_MAPPED_TEXTURE2D, D3D10_MAPPED_TEXTURE2D structure [Direct3D 10], a2002d27-1e59-abab-3507-86a1666a3405, d3d10/D3D10_MAPPED_TEXTURE2D, direct3d10.d3d10_mapped_texture2d
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: D3D10_MAPPED_TEXTURE2D
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_MAPPED_TEXTURE2D
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_MAPPED_TEXTURE2D structure


## -description


Provides access to <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresource</a> data in a 2D texture.


## -struct-fields




### -field pData

Type: <b>void*</b>

Pointer to the data.


### -field RowPitch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The pitch, or width, or physical size (in bytes), of one row of an uncompressed texture. A block-compressed texture is encoded in 4x4 blocks (see <a href="https://msdn.microsoft.com/add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5">virtual size vs physical size</a>) ; therefore, <b>RowPitch</b> is the number of bytes in a block of 4x4 texels.


## -remarks



This structure is used in a call to <a href="https://msdn.microsoft.com/40d0d246-bed9-48a2-9c00-68a5c58f49a5">Map</a>.

To illustrate the row pitch, assume an uncompressed 2D texture with mipmap levels, as shown in the following illustration.

<img alt="Illustration of an uncompressed 2D texture with mipmap levels" src="/images/d3d10_resource_texture2d.png"/>

Visualize the top-level texture drawn in a single plane like the following illustration.

<img alt="Illustration of a single plane" src="/images/d3d10_2d_texture_conceptual.png"/>

However, the actual layout of each element in memory looks more like the following illustration.

<img alt="Illustration of the row pitch in memory" src="/images/d3d10_2d_texture_memory.png"/>

For this example, the row pitch encompasses 5 elements (one row), whose size would be five times the number of bytes per element.

Use row pitch to advance a pointer between rows within a single 2D texture plane.

<h3><a id="Example"></a><a id="example"></a><a id="EXAMPLE"></a>Example</h3>
To access data in, say, the third mipmap level, you must cast the <b>pData</b> pointer as demonstrated in the following example for a floating-point texture.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
D3D10_MAPPED_TEXTURE2D mappedTexture;
if( SUCCEEDED( pTexture-&gt;Map( D3D10CalcSubresource(2, 0, 3), D3D10_MAP_WRITE_DISCARD, 0, &amp;mappedTexture )))
{
    D3D10_TEXTURE2D_DESC desc;
    pTexture-&gt;GetDesc( &amp;desc );
	
    // Compute the width and height of the third mipmap level
    const UINT WIDTH = desc.Width &gt;&gt; 2;
    const UINT HEIGHT = desc.Height &gt;&gt; 2;
	
    FLOAT* pTexels = (FLOAT*)mappedTexture.pData;
    for( UINT row = 0; row &lt; HEIGHT; row++ )
    {
      UINT rowStart = row * mappedTexture.RowPitch/4;
      for( UINT col = 0; col &lt; WIDTH; col++ )
      {
        pTexels[rowStart + col*4 + 0]; // Red
        pTexels[rowStart + col*4 + 1]; // Green
        pTexels[rowStart + col*4 + 2]; // Blue
        pTexels[rowStart + col*4 + 3]; // Alpha
      }
    }

    pTexture-&gt;Unmap(D3D10CalcSubresource(2, 0, 3));
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d8fe2ebe-349a-456e-9a5a-16f2d3419800">Resource Structures</a>
 

 

