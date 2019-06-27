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
f1_keywords: 
 - "dcomp/IDCompositionRectangleClip"
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionRectangleClip</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionclip">IDCompositionClip</a>. <b>IDCompositionRectangleClip</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setbottom">SetBottom</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Bottom property of a clip rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setbottomleftradiusx">SetBottomLeftRadiusX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the BottomLeftRadiusX property of this clip. The BottomLeftRadiusX property  specifies the x radius of the ellipse that rounds the lower-left corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setbottomleftradiusy">SetBottomLeftRadiusY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the BottomLeftRadiusY property of this clip. The BottomLeftRadiusY property  specifies the y radius of the ellipse that rounds the lower-left corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setbottomrightradiusx">SetBottomRightRadiusX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the BottomRightRadiusX property of this clip. The BottomRightRadiusX property  specifies the x radius of the ellipse that rounds the lower-right corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setbottomrightradiusy">SetBottomRightRadiusY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the BottomRightRadiusY property of this clip. The BottomRightRadiusY property  specifies the y radius of the ellipse that rounds the lower-right corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setleft">SetLeft</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Left property of a clip rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setright">SetRight</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Right property of a clip rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-settop">SetTop</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Top property of a clip rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-settopleftradiusx">SetTopLeftRadiusX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the TopLeftRadiusX property of this clip. The TopLeftRadiusX property  specifies the x radius of the ellipse that rounds the top-left corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-settopleftradiusy">SetTopLeftRadiusY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the TopLeftRadiusY property of this clip. The TopLeftRadiusY property  specifies the y radius of the ellipse that rounds the top-left corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-settoprightradiusx">SetTopRightRadiusX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the TopRightRadiusX property of this clip. The TopRightRadiusX property  specifies the x radius of the ellipse that rounds the top-right corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-settoprightradiusy">SetTopRightRadiusY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the TopRightRadiusY property of this clip. The TopRightRadiusY property  specifies the y radius of the ellipse that rounds the top-right corner of the clip.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionclip">IDCompositionClip</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-setclip">IDCompositionVisual::SetClip</a>
 

 

