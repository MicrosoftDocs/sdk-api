---
UID: NN:d2d1_3.ID2D1DeviceContext2
title: ID2D1DeviceContext2 (d2d1_3.h)
description: This interface performs all the same functions as the ID2D1DeviceContext1 interface, plus it enables functionality such as ink rendering, gradient mesh rendering, and improved image loading.
helpviewer_keywords: ["ID2D1DeviceContext2","ID2D1DeviceContext2 interface [Direct2D]","ID2D1DeviceContext2 interface [Direct2D]","described","d2d1_3/ID2D1DeviceContext2","direct2d.id2d1devicecontext2"]
old-location: direct2d\id2d1devicecontext2.htm
tech.root: Direct2D
ms.assetid: 25c11cfc-75af-20a1-8f54-6b370942b841
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext2, ID2D1DeviceContext2 interface [Direct2D], ID2D1DeviceContext2 interface [Direct2D],described, d2d1_3/ID2D1DeviceContext2, direct2d.id2d1devicecontext2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext2
 - d2d1_3/ID2D1DeviceContext2
dev_langs:
 - c++
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
---

# ID2D1DeviceContext2 interface


## -description

This interface performs all the same functions as the ID2D1DeviceContext1 interface, plus it enables functionality such as ink rendering, gradient mesh rendering, and improved image loading.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DeviceContext2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1devicecontext1">ID2D1DeviceContext1</a>. <b>ID2D1DeviceContext2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-creategradientmesh">CreateGradientMesh</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1gradientmesh">ID2D1GradientMesh</a> instance using the given array of patches.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi">CreateImageSourceFromDxgi</a>
</td>
<td align="left" width="63%">
Creates an image source from a set of DXGI surface(s).  The YCbCr surface(s) are converted to RGBA automatically during subsequent drawing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-createimagesourcefromwic">CreateImageSourceFromWic</a>
</td>
<td align="left" width="63%">Overloaded. Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source.  The image is loaded and stored while using a minimal amount of memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-createink">CreateInk</a>
</td>
<td align="left" width="63%">Overloaded. Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1ink">ID2D1Ink</a> object that starts at the given point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-createinkstyle">CreateInkStyle</a>
</td>
<td align="left" width="63%">Overloaded. Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1inkstyle">ID2D1InkStyle</a> object, for use with ink 
        rendering methods such as <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink">DrawInk</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createlookuptable3d">CreateLookupTable3D</a>
</td>
<td align="left" width="63%">
Creates a 3D lookup table for mapping a 3-channel input to a 3-channel output. The table data must be provided in 4-channel format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createtransformedimagesource">CreateTransformedImageSource</a>
</td>
<td align="left" width="63%">
Creates an image source which shares resources with an original.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1devicecontext2-drawgdimetafile-overload">DrawGdiMetafile</a>
</td>
<td align="left" width="63%">Overloaded. Draw a metafile to the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawgradientmesh">DrawGradientMesh</a>
</td>
<td align="left" width="63%">
Renders a given gradient mesh to the target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink">DrawInk</a>
</td>
<td align="left" width="63%">
Renders the given ink object using the given brush and ink style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-getgradientmeshworldbounds">GetGradientMeshWorldBounds</a>
</td>
<td align="left" width="63%">
Returns the world bounds of a given gradient mesh.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1devicecontext1">ID2D1DeviceContext1</a>

