---
UID: NN:dcomp.IDCompositionVirtualSurface
title: IDCompositionVirtualSurface (dcomp.h)
description: Represents a sparsely allocated bitmap that can be associated with a visual for composition in a visual tree.
old-location: directcomp\idcompositionvirtualsurface.htm
tech.root: directcomp
ms.assetid: 51E8D52C-2446-46B6-A5C1-0DC7FA9DF4CC
ms.date: 12/05/2018
ms.keywords: IDCompositionVirtualSurface, IDCompositionVirtualSurface interface [DirectComposition], IDCompositionVirtualSurface interface [DirectComposition],described, dcomp/IDCompositionVirtualSurface, directcomp.idcompositionvirtualsurface
ms.topic: interface
f1_keywords:
- dcomp/IDCompositionVirtualSurface
dev_langs:
- c++
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
- IDCompositionVirtualSurface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionVirtualSurface interface


## -description


Represents a sparsely allocated bitmap that can be associated with a visual for composition in a visual tree.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionVirtualSurface</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionsurface">IDCompositionSurface</a>. <b>IDCompositionVirtualSurface</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionVirtualSurface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvirtualsurface-resize">Resize</a>
</td>
<td align="left" width="63%">
Changes the logical size of this virtual surface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim">Trim</a>
</td>
<td align="left" width="63%">
Discards pixels that fall outside of the specified trim rectangles.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionsurface">IDCompositionSurface</a>
 

 

