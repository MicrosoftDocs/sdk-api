---
UID: NN:dcomp.IDCompositionSurfaceFactory
title: IDCompositionSurfaceFactory (dcomp.h)
description: Creates surface and virtual surface objects associated with an application-provided rendering device.
helpviewer_keywords: ["IDCompositionSurfaceFactory","IDCompositionSurfaceFactory interface [DirectComposition]","IDCompositionSurfaceFactory interface [DirectComposition]","described","dcomp/IDCompositionSurfaceFactory","directcomp.idcompositionsurfacefactory"]
old-location: directcomp\idcompositionsurfacefactory.htm
tech.root: directcomp
ms.assetid: 1BB028E0-376E-42BD-82FD-08331341C93B
ms.date: 12/05/2018
ms.keywords: IDCompositionSurfaceFactory, IDCompositionSurfaceFactory interface [DirectComposition], IDCompositionSurfaceFactory interface [DirectComposition],described, dcomp/IDCompositionSurfaceFactory, directcomp.idcompositionsurfacefactory
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionSurfaceFactory
 - dcomp/IDCompositionSurfaceFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionSurfaceFactory
---

# IDCompositionSurfaceFactory interface


## -description

Creates surface and virtual surface objects associated with an application-provided rendering device.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionSurfaceFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDCompositionSurfaceFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionSurfaceFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurfacefactory-createsurface">CreateSurface</a>
</td>
<td align="left" width="63%">
Creates a surface object that can be associated with one or more visuals for composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurfacefactory-createvirtualsurface">CreateVirtualSurface</a>
</td>
<td align="left" width="63%">
Creates a sparsely populated surface that can be associated with one or more visuals for composition.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionsurface">IDCompositionSurface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionvirtualsurface">IDCompositionVirtualSurface</a>

