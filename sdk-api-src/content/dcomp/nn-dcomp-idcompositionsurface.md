---
UID: NN:dcomp.IDCompositionSurface
title: IDCompositionSurface
author: windows-sdk-content
description: Represents a physical bitmap that can be associated with a visual for composition in a visual tree. This interface can also be used to update the bitmap contents.
old-location: directcomp\idcompositionsurface.htm
tech.root: directcomp
ms.assetid: E271B4DC-5F09-426A-A5D3-43A48F30CB24
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionSurface, IDCompositionSurface interface [DirectComposition], IDCompositionSurface interface [DirectComposition],described, dcomp/IDCompositionSurface, directcomp.idcompositionsurface
ms.prod: windows
ms.technology: windows-sdk
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
 - IDCompositionSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionSurface interface


## -description


Represents a physical bitmap that can be associated with a visual for composition in a visual tree.  This interface can also be used to update the bitmap contents. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionSurface</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDCompositionSurface</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionSurface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0D7E90A1-90E4-44BE-A4DA-8DA300C81A35">BeginDraw</a>
</td>
<td align="left" width="63%">
Initiates drawing on this DirectComposition surface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/127195F7-6000-4D8C-B850-3E4D40BC4082">EndDraw</a>
</td>
<td align="left" width="63%">
Marks the end of drawing on this DirectComposition surface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EE008AAB-0C79-4D60-953C-7A9BCFED2C41">ResumeDraw</a>
</td>
<td align="left" width="63%">
Resumes drawing on this DirectComposition surface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0764C59A-DDDE-420C-B044-827B7EDC6CF1">Scroll</a>
</td>
<td align="left" width="63%">
Scrolls a rectangular area of a DirectComposition logical surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B3CD2007-502C-48EF-989E-4C690B2B65D8">SuspendDraw</a>
</td>
<td align="left" width="63%">
Suspends the drawing on this DirectComposition surface object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/550BA10B-D582-4A57-A69D-3EFFC7313D8F">DCompositionCreateSurfaceHandle</a>



<a href="https://msdn.microsoft.com/51E8D52C-2446-46B6-A5C1-0DC7FA9DF4CC">IDCompositionVirtualSurface</a>



<a href="https://msdn.microsoft.com/894E6E30-6C28-476D-9AE5-D0664A69E03C">IDCompositionVisual::SetContent</a>
 

 

