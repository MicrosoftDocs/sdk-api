---
UID: NN:d2d1_3.ID2D1DeviceContext2
title: ID2D1DeviceContext2
author: windows-sdk-content
description: This interface performs all the same functions as the ID2D1DeviceContext1 interface, plus it enables functionality such as ink rendering, gradient mesh rendering, and improved image loading.
old-location: direct2d\id2d1devicecontext2.htm
tech.root: Direct2D
ms.assetid: 25c11cfc-75af-20a1-8f54-6b370942b841
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID2D1DeviceContext2, ID2D1DeviceContext2 interface [Direct2D], ID2D1DeviceContext2 interface [Direct2D],described, d2d1_3/ID2D1DeviceContext2, direct2d.id2d1devicecontext2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - ID2D1DeviceContext2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext2 interface


## -description


This interface performs all the same functions as the ID2D1DeviceContext1 interface, plus it enables functionality such as ink rendering, gradient mesh rendering, and improved image loading.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DeviceContext2</b> interface inherits from <a href="https://msdn.microsoft.com/E08FDAE4-05D3-472C-9AD9-228BAF989F1D">ID2D1DeviceContext1</a>. <b>ID2D1DeviceContext2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1DeviceContext2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c471ba3-fb0f-b735-d10b-9d0a56b32863">CreateGradientMesh</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/0c51da97-7b70-d828-2a4d-cb62ff378a56">ID2D1GradientMesh</a> instance using the given array of patches.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ea6ba4c-9bd6-a909-82d5-c4690dc9a24e">CreateImageSourceFromDxgi</a>
</td>
<td align="left" width="63%">
Creates an image source from a set of DXGI surface(s).  The YCbCr surface(s) are converted to RGBA automatically during subsequent drawing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af02630d-a9ca-f5b4-6f2a-31a73ef603e5">CreateImageSourceFromWic</a>
</td>
<td align="left" width="63%">Overloaded. Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source.  The image is loaded and stored while using a minimal amount of memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e79b7cc-a6c4-72e3-d3d4-8346b19feac5">CreateInk</a>
</td>
<td align="left" width="63%">Overloaded. Creates a new <a href="https://msdn.microsoft.com/4B6DD4C2-8E91-4AEA-AFB5-21B4FD13F75A">ID2D1Ink</a> object that starts at the given point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/647cf483-c650-4a6a-a1cd-272f3af0e6b6">CreateInkStyle</a>
</td>
<td align="left" width="63%">Overloaded. Creates a new <a href="https://msdn.microsoft.com/03853FA5-1377-42FB-A4C2-50069DDF6E2D">ID2D1InkStyle</a> object, for use with ink 
        rendering methods such as <a href="https://msdn.microsoft.com/d7c27267-c0c3-d21c-7980-3d92396509c7">DrawInk</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c48804b-9876-9dbd-3d20-8a7b575fd3d8">CreateLookupTable3D</a>
</td>
<td align="left" width="63%">
Creates a 3D lookup table for mapping a 3-channel input to a 3-channel output. The table data must be provided in 4-channel format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ABA6A8E-B691-47FF-AE32-1FC5D29C48B2">CreateTransformedImageSource</a>
</td>
<td align="left" width="63%">
Creates an image source which shares resources with an original.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c093da19-9def-115c-9e2f-d8f4d98aee92">DrawGdiMetafile</a>
</td>
<td align="left" width="63%">Overloaded. Draw a metafile to the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3ea0930-2e7c-8e28-eda0-7dcb0b1cccc8">DrawGradientMesh</a>
</td>
<td align="left" width="63%">
Renders a given gradient mesh to the target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7c27267-c0c3-d21c-7980-3d92396509c7">DrawInk</a>
</td>
<td align="left" width="63%">
Renders the given ink object using the given brush and ink style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/809d851c-a3e0-7609-95e0-637e25cdaa06">GetGradientMeshWorldBounds</a>
</td>
<td align="left" width="63%">
Returns the world bounds of a given gradient mesh.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/E08FDAE4-05D3-472C-9AD9-228BAF989F1D">ID2D1DeviceContext1</a>
 

 

