---
UID: NF:d3d11_1.ID3D11DeviceContext1.ClearView
title: ID3D11DeviceContext1::ClearView (d3d11_1.h)
description: Sets all the elements in a resource view to one value.
helpviewer_keywords: ["ClearView","ClearView method [Direct3D 11]","ClearView method [Direct3D 11]","ID3D11DeviceContext1 interface","ID3D11DeviceContext1 interface [Direct3D 11]","ClearView method","ID3D11DeviceContext1.ClearView","ID3D11DeviceContext1::ClearView","d3d11_1/ID3D11DeviceContext1::ClearView","direct3d11.id3d11devicecontext1_clearview"]
old-location: direct3d11\id3d11devicecontext1_clearview.htm
tech.root: direct3d11
ms.assetid: 7CC8DEB6-075C-40EB-822D-8A627E285FA2
ms.date: 12/05/2018
ms.keywords: ClearView, ClearView method [Direct3D 11], ClearView method [Direct3D 11],ID3D11DeviceContext1 interface, ID3D11DeviceContext1 interface [Direct3D 11],ClearView method, ID3D11DeviceContext1.ClearView, ID3D11DeviceContext1::ClearView, d3d11_1/ID3D11DeviceContext1::ClearView, direct3d11.id3d11devicecontext1_clearview
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11DeviceContext1::ClearView
 - d3d11_1/ID3D11DeviceContext1::ClearView
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
 - ID3D11DeviceContext1.ClearView
---

# ID3D11DeviceContext1::ClearView


## -description

Sets all the elements in a resource view to one value.

## -parameters

### -param pView [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a> interface that represents the resource view to clear.

### -param Color [in]

A 4-component array that represents the color to use to clear the resource view.

### -param pRect [in, optional]

An array of <a href="/windows/desktop/direct3d11/d3d11-rect">D3D11_RECT</a> structures for the rectangles in the resource view to clear. If <b>NULL</b>, <b>ClearView</b> clears the entire surface.

### -param NumRects

Number of rectangles in the array that the  <i>pRect</i> parameter specifies.

## -remarks

<b>ClearView</b> works only on render-target views (RTVs), depth/stencil views (DSVs) on depth-only resources (resources with no stencil component), unordered-access views (UAVs), or any video view of a <a href="/windows/desktop/direct3dhlsl/sm5-object-texture2d">Texture2D</a> surface. The runtime drops invalid calls. Empty rectangles in the <i>pRect</i> array are a no-op. A rectangle is empty if the top value equals the bottom value or the left value equals the right value.

<b>ClearView</b> doesn’t support 3D textures.

<b>ClearView</b> applies the same color value to all array slices in a view; all rectangles in the <i>pRect</i> array correspond to each array slice.  The <i>pRect</i> array of rectangles is a set of areas to clear on a single surface.  If the view is an array, <b>ClearView</b> clears all the rectangles on each array slice individually.

When you apply rectangles to buffers, set the top value to 0 and the bottom value to 1 and set the left value and right value to describe the extent within the buffer. When the top value equals the bottom value or the left value equals the right value, the rectangle is empty and a no-op is achieved.

The driver converts and clamps color values to the destination format as appropriate per Direct3D conversion rules.  For example, if the format of the view is <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_R8G8B8A8_UNORM</a>, the driver clamps inputs to 0.0f to 1.0f (+INF -&gt; 1.0f (0XFF)/NaN -&gt; 0.0f).

If the format is integer, such as <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_R8G8B8A8_UINT</a>, the runtime interprets inputs as integral floats. Therefore, 235.0f maps to 235 (rounds to zero, out of range/INF values clamp to target range, and NaN to 0).

Here are the color mappings:

<ul>
<li>Color[0]: R (or Y for video)</li>
<li>Color[1]: G (or U/Cb for video)</li>
<li>Color[2]: B (or V/Cr for video)</li>
<li>Color[3]: A</li>
</ul>
For video views with YUV or YCbBr formats, <b>ClearView</b> doesn't convert color values. In situations where the format name doesn’t indicate _UNORM,  _UINT, and so on, <b>ClearView</b> assumes _UINT. Therefore, 235.0f maps to 235 (rounds to zero, out of range/INF values clamp to target range, and NaN to 0).

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a>