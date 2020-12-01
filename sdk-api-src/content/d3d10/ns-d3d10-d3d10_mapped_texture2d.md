---
UID: NS:d3d10.D3D10_MAPPED_TEXTURE2D
title: D3D10_MAPPED_TEXTURE2D (d3d10.h)
description: Provides access to subresource data in a 2D texture.
helpviewer_keywords: ["D3D10_MAPPED_TEXTURE2D","D3D10_MAPPED_TEXTURE2D structure [Direct3D 10]","a2002d27-1e59-abab-3507-86a1666a3405","d3d10/D3D10_MAPPED_TEXTURE2D","direct3d10.d3d10_mapped_texture2d"]
old-location: direct3d10\d3d10_mapped_texture2d.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_mapped_texture2d.htm
ms.date: 12/05/2018
ms.keywords: D3D10_MAPPED_TEXTURE2D, D3D10_MAPPED_TEXTURE2D structure [Direct3D 10], a2002d27-1e59-abab-3507-86a1666a3405, d3d10/D3D10_MAPPED_TEXTURE2D, direct3d10.d3d10_mapped_texture2d
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D10_MAPPED_TEXTURE2D
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_MAPPED_TEXTURE2D
 - d3d10/D3D10_MAPPED_TEXTURE2D
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_MAPPED_TEXTURE2D
---

# D3D10_MAPPED_TEXTURE2D structure


## -description

Provides access to <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource</a> data in a 2D texture.

## -struct-fields

### -field pData

Type: <b>void*</b>

Pointer to the data.

### -field RowPitch

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The pitch, or width, or physical size (in bytes), of one row of an uncompressed texture. A block-compressed texture is encoded in 4x4 blocks (see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">virtual size vs physical size</a>) ; therefore, <b>RowPitch</b> is the number of bytes in a block of 4x4 texels.

## -remarks

This structure is used in a call to <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10texture2d-map">Map</a>.

To illustrate the row pitch, assume an uncompressed 2D texture with mipmap levels, as shown in the following illustration.

<img alt="Illustration of an uncompressed 2D texture with mipmap levels" src="./images/d3d10_resource_texture2d.png"/>

Visualize the top-level texture drawn in a single plane like the following illustration.

<img alt="Illustration of a single plane" src="./images/d3d10_2d_texture_conceptual.png"/>

However, the actual layout of each element in memory looks more like the following illustration.

<img alt="Illustration of the row pitch in memory" src="./images/d3d10_2d_texture_memory.png"/>

For this example, the row pitch encompasses 5 elements (one row), whose size would be five times the number of bytes per element.

Use row pitch to advance a pointer between rows within a single 2D texture plane.

<h3><a id="Example"></a><a id="example"></a><a id="EXAMPLE"></a>Example</h3>
To access data in, say, the third mipmap level, you must cast the <b>pData</b> pointer as demonstrated in the following example for a floating-point texture.


```

D3D10_MAPPED_TEXTURE2D mappedTexture;
if( SUCCEEDED( pTexture->Map( D3D10CalcSubresource(2, 0, 3), D3D10_MAP_WRITE_DISCARD, 0, &mappedTexture )))
{
    D3D10_TEXTURE2D_DESC desc;
    pTexture->GetDesc( &desc );
	
    // Compute the width and height of the third mipmap level
    const UINT WIDTH = desc.Width >> 2;
    const UINT HEIGHT = desc.Height >> 2;
	
    FLOAT* pTexels = (FLOAT*)mappedTexture.pData;
    for( UINT row = 0; row < HEIGHT; row++ )
    {
      UINT rowStart = row * mappedTexture.RowPitch/4;
      for( UINT col = 0; col < WIDTH; col++ )
      {
        pTexels[rowStart + col*4 + 0]; // Red
        pTexels[rowStart + col*4 + 1]; // Green
        pTexels[rowStart + col*4 + 2]; // Blue
        pTexels[rowStart + col*4 + 3]; // Alpha
      }
    }

    pTexture->Unmap(D3D10CalcSubresource(2, 0, 3));
}

```

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>