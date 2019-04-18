---
UID: NN:dcomp.IDCompositionRectangleClip
title: IDCompositionRectangleClip (dcomp.h)
author: windows-sdk-content
description: Represents a clip object that restricts the rendering of a visual subtree to the specified rectangular region. Optionally, the clip object may have rounded corners specified.
old-location: directcomp\idcompositionrectangleclip.htm
tech.root: directcomp
ms.assetid: 486bcdb9-e353-4ca2-b24c-af863dda7470
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionRectangleClip, IDCompositionRectangleClip interface [DirectComposition], IDCompositionRectangleClip interface [DirectComposition],described, dcomp/IDCompositionRectangleClip, directcomp.idcompositionrectangleclip
ms.topic: interface
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionRectangleClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionRectangleClip interface


## -description


Represents a clip object that restricts the rendering of a visual subtree to the specified rectangular region. Optionally, the clip object may have rounded corners specified.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionRectangleClip</b> interface inherits from <a href="https://msdn.microsoft.com/647638f4-7eca-42bc-a083-3d9d15089648">IDCompositionClip</a>. <b>IDCompositionRectangleClip</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionRectangleClip</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh448897(v=VS.85).aspx">SetBottom</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Bottom property of a clip rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh437435(v=VS.85).aspx">SetBottomLeftRadiusX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the BottomLeftRadiusX property of this clip. The BottomLeftRadiusX property  specifies the x radius of the ellipse that rounds the lower-left corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh437441(v=VS.85).aspx">SetBottomLeftRadiusY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the BottomLeftRadiusY property of this clip. The BottomLeftRadiusY property  specifies the y radius of the ellipse that rounds the lower-left corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh448849(v=VS.85).aspx">SetBottomRightRadiusX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the BottomRightRadiusX property of this clip. The BottomRightRadiusX property  specifies the x radius of the ellipse that rounds the lower-right corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh448854(v=VS.85).aspx">SetBottomRightRadiusY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the BottomRightRadiusY property of this clip. The BottomRightRadiusY property  specifies the y radius of the ellipse that rounds the lower-right corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh448903(v=VS.85).aspx">SetLeft</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Left property of a clip rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh448908(v=VS.85).aspx">SetRight</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Right property of a clip rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh448923(v=VS.85).aspx">SetTop</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Top property of a clip rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh448909(v=VS.85).aspx">SetTopLeftRadiusX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the TopLeftRadiusX property of this clip. The TopLeftRadiusX property  specifies the x radius of the ellipse that rounds the top-left corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh448912(v=VS.85).aspx">SetTopLeftRadiusY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the TopLeftRadiusY property of this clip. The TopLeftRadiusY property  specifies the y radius of the ellipse that rounds the top-left corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh448915(v=VS.85).aspx">SetTopRightRadiusX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the TopRightRadiusX property of this clip. The TopRightRadiusX property  specifies the x radius of the ellipse that rounds the top-right corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh448918(v=VS.85).aspx">SetTopRightRadiusY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the TopRightRadiusY property of this clip. The TopRightRadiusY property  specifies the y radius of the ellipse that rounds the top-right corner of the clip.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/647638f4-7eca-42bc-a083-3d9d15089648">IDCompositionClip</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449155(v=VS.85).aspx">IDCompositionVisual::SetClip</a>
 

 

