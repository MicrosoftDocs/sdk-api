---
UID: NN:dcomp.IDCompositionFilterEffect
title: IDCompositionFilterEffect (dcomp.h)
description: Represents a filter effect.helpviewer_keywords: ["IDCompositionFilterEffect","IDCompositionFilterEffect interface [DirectComposition]","IDCompositionFilterEffect interface [DirectComposition]","described","dcomp/IDCompositionFilterEffect","directcomp.idcompositionfiltereffect"]
old-location: directcomp\idcompositionfiltereffect.htm
tech.root: directcomp
ms.assetid: 4303c24d-e3e1-e188-bbef-e654c0e7e266
ms.date: 12/05/2018
ms.keywords: IDCompositionFilterEffect, IDCompositionFilterEffect interface [DirectComposition], IDCompositionFilterEffect interface [DirectComposition],described, dcomp/IDCompositionFilterEffect, directcomp.idcompositionfiltereffect
f1_keywords:
- dcomp/IDCompositionFilterEffect
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
- IDCompositionFilterEffect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionFilterEffect interface


## -description


Represents a filter effect.

IDCompositionFilterEffect exposes a subset of Direct2D's image <a href="https://docs.microsoft.com/windows/desktop/Direct2D/effects-overview">effects</a> through Direction Composition for use in CSS filters in the browser platform.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionFilterEffect</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffect">IDCompositionEffect</a>. <b>IDCompositionFilterEffect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionFilterEffect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionfiltereffect-setinput">SetInput</a>
</td>
<td align="left" width="63%">
Sets the the input at an index to the specified filter effect.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffect">IDCompositionEffect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>
 

 

