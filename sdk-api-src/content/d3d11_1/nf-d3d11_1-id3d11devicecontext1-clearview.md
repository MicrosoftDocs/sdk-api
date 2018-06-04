---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D11DeviceContext1::ClearView


## -description


Sets all the elements in a resource view to one value.


## -parameters




### -param pView [in]

A pointer to the <a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a> interface that represents the resource view to clear.


### -param Color [in]

A 4-component array that represents the color to use to clear the resource view.


### -param pRect [in, optional]

An array of <a href="https://msdn.microsoft.com/d1cbbbd7-1221-4706-b805-8422c5ebdadc">D3D11_RECT</a> structures for the rectangles in the resource view to clear. If <b>NULL</b>, <b>ClearView</b> clears the entire surface.


### -param NumRects

Number of rectangles in the array that the  <i>pRect</i> parameter specifies.


## -returns



Returns nothing.




## -remarks



<b>ClearView</b> works only on render-target views (RTVs), depth/stencil views (DSVs) on depth-only resources (resources with no stencil component), unordered-access views (UAVs), or any video view of a <a href="https://msdn.microsoft.com/e4f9cfd8-65e6-4375-8f87-736bca32cad4">Texture2D</a> surface. The runtime drops invalid calls. Empty rectangles in the <i>pRect</i> array are a no-op. A rectangle is empty if the top value equals the bottom value or the left value equals the right value.

<b>ClearView</b> doesn’t support 3D textures.

<b>ClearView</b> applies the same color value to all array slices in a view; all rectangles in the <i>pRect</i> array correspond to each array slice.  The <i>pRect</i> array of rectangles is a set of areas to clear on a single surface.  If the view is an array, <b>ClearView</b> clears all the rectangles on each array slice individually.

When you apply rectangles to buffers, set the top value to 0 and the bottom value to 1 and set the left value and right value to describe the extent within the buffer. When the top value equals the bottom value or the left value equals the right value, the rectangle is empty and a no-op is achieved.

The driver converts and clamps color values to the destination format as appropriate per Direct3D conversion rules.  For example, if the format of the view is <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R8G8B8A8_UNORM</a>, the driver clamps inputs to 0.0f to 1.0f (+INF -&gt; 1.0f (0XFF)/NaN -&gt; 0.0f).

If the format is integer, such as <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R8G8B8A8_UINT</a>, the runtime interprets inputs as integral floats. Therefore, 235.0f maps to 235 (rounds to zero, out of range/INF values clamp to target range, and NaN to 0).

Here are the color mappings:

<ul>
<li>Color[0]: R (or Y for video)</li>
<li>Color[1]: G (or U/Cb for video)</li>
<li>Color[2]: B (or V/Cr for video)</li>
<li>Color[3]: A</li>
</ul>
For video views with YUV or YCbBr formats, <b>ClearView</b> doesn't convert color values. In situations where the format name doesn’t indicate _UNORM,  _UINT, and so on, <b>ClearView</b> assumes _UINT. Therefore, 235.0f maps to 235 (rounds to zero, out of range/INF values clamp to target range, and NaN to 0).




## -see-also




<a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a>
 

 

