---
UID: NN:dcomp.IDCompositionSurface
title: IDCompositionSurface (dcomp.h)
author: windows-sdk-content
description: Represents a physical bitmap that can be associated with a visual for composition in a visual tree. This interface can also be used to update the bitmap contents.
old-location: directcomp\idcompositionsurface.htm
tech.root: directcomp
ms.assetid: E271B4DC-5F09-426A-A5D3-43A48F30CB24
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionSurface, IDCompositionSurface interface [DirectComposition], IDCompositionSurface interface [DirectComposition],described, dcomp/IDCompositionSurface, directcomp.idcompositionsurface
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
ms.custom: 19H1
---

# IDCompositionSurface interface


## -description


Represents a physical bitmap that can be associated with a visual for composition in a visual tree.  This interface can also be used to update the bitmap contents. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionSurface</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDCompositionSurface</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-begindraw">BeginDraw</a>
</td>
<td align="left" width="63%">
Initiates drawing on this DirectComposition surface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-enddraw">EndDraw</a>
</td>
<td align="left" width="63%">
Marks the end of drawing on this DirectComposition surface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw">ResumeDraw</a>
</td>
<td align="left" width="63%">
Resumes drawing on this DirectComposition surface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-scroll">Scroll</a>
</td>
<td align="left" width="63%">
Scrolls a rectangular area of a DirectComposition logical surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw">SuspendDraw</a>
</td>
<td align="left" width="63%">
Suspends the drawing on this DirectComposition surface object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle">DCompositionCreateSurfaceHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionvirtualsurface">IDCompositionVirtualSurface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-setcontent">IDCompositionVisual::SetContent</a>
 

 

