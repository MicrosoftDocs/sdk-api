---
UID: NN:dcomp.IDCompositionRectangleClip
title: IDCompositionRectangleClip
author: windows-sdk-content
description: Represents a clip object that restricts the rendering of a visual subtree to the specified rectangular region. Optionally, the clip object may have rounded corners specified.
old-location: directcomp\idcompositionrectangleclip.htm
tech.root: directcomp
ms.assetid: 486bcdb9-e353-4ca2-b24c-af863dda7470
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionRectangleClip, IDCompositionRectangleClip interface [DirectComposition], IDCompositionRectangleClip interface [DirectComposition],described, dcomp/IDCompositionRectangleClip, directcomp.idcompositionrectangleclip
ms.prod: windows-hardware
ms.technology: windows-devices
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
<a href="https://msdn.microsoft.com/5C80AA94-AE61-4F12-86C8-6474ADD455B1">SetBottom</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Bottom property of a clip rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1E008D8E-B28A-4E79-9653-587DF0CB5DD7">SetBottomLeftRadiusX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the BottomLeftRadiusX property of this clip. The BottomLeftRadiusX property  specifies the x radius of the ellipse that rounds the lower-left corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/299D718D-F313-4884-B89B-8CE5EBF78B74">SetBottomLeftRadiusY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the BottomLeftRadiusY property of this clip. The BottomLeftRadiusY property  specifies the y radius of the ellipse that rounds the lower-left corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/036E842C-320B-4C6B-9D83-561B2A107A59">SetBottomRightRadiusX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the BottomRightRadiusX property of this clip. The BottomRightRadiusX property  specifies the x radius of the ellipse that rounds the lower-right corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A2A3F43E-62C6-43B8-929F-AEDA11620DF1">SetBottomRightRadiusY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the BottomRightRadiusY property of this clip. The BottomRightRadiusY property  specifies the y radius of the ellipse that rounds the lower-right corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A8E2C2A3-6146-486F-8FF4-05097BFE9222">SetLeft</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Left property of a clip rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DBF1C6CE-5256-4175-9530-30D0B24FAB6D">SetRight</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Right property of a clip rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32C12765-F580-4E32-9C48-3A7AFD95CA38">SetTop</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Top property of a clip rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75168197-FA76-4B57-AF24-C92DF2602985">SetTopLeftRadiusX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the TopLeftRadiusX property of this clip. The TopLeftRadiusX property  specifies the x radius of the ellipse that rounds the top-left corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D188BCD0-00F2-406D-BF69-33E8E37C8E6B">SetTopLeftRadiusY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the TopLeftRadiusY property of this clip. The TopLeftRadiusY property  specifies the y radius of the ellipse that rounds the top-left corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2FCE8558-2EED-4A44-93F3-796984C47AF0">SetTopRightRadiusX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the TopRightRadiusX property of this clip. The TopRightRadiusX property  specifies the x radius of the ellipse that rounds the top-right corner of the clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CB0C1B66-F1AB-4440-8898-77107C1A2C42">SetTopRightRadiusY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the TopRightRadiusY property of this clip. The TopRightRadiusY property  specifies the y radius of the ellipse that rounds the top-right corner of the clip.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/647638f4-7eca-42bc-a083-3d9d15089648">IDCompositionClip</a>



<a href="https://msdn.microsoft.com/ACEBA4F9-E1B0-459B-8DC2-272A822AB214">IDCompositionVisual::SetClip</a>
 

 

