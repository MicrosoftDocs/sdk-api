---
UID: NN:dcomp.IDCompositionTranslateTransform
title: IDCompositionTranslateTransform (dcomp.h)
description: Represents a 2D transformation that affects only the offset of a visual along the x-axis and y-axis.
helpviewer_keywords: ["IDCompositionTranslateTransform","IDCompositionTranslateTransform interface [DirectComposition]","IDCompositionTranslateTransform interface [DirectComposition]","described","dcomp/IDCompositionTranslateTransform","directcomp.idcompositiontranslatetransform"]
old-location: directcomp\idcompositiontranslatetransform.htm
tech.root: directcomp
ms.assetid: 2215721e-a10d-4c9e-b5b7-1698afa547d8
ms.date: 12/05/2018
ms.keywords: IDCompositionTranslateTransform, IDCompositionTranslateTransform interface [DirectComposition], IDCompositionTranslateTransform interface [DirectComposition],described, dcomp/IDCompositionTranslateTransform, directcomp.idcompositiontranslatetransform
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionTranslateTransform
 - dcomp/IDCompositionTranslateTransform
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
 - IDCompositionTranslateTransform
---

# IDCompositionTranslateTransform interface


## -description

Represents a 2D transformation that affects only the offset of a visual along the x-axis and y-axis.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionTranslateTransform</b> interface inherits from <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>. <b>IDCompositionTranslateTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionTranslateTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/hh449126(v=vs.85)">SetOffsetX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the OffsetX property of a 2D translation transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/hh449131(v=vs.85)">SetOffsetY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the OffsetY property of a 2D translation transform.

</td>
</tr>
</table>

## -remarks

A translation transform represents the following 3-by-2 matrix:

<img alt="Three-by-two translation matrix" src="./images/translate_transform_3x2matrix.png"/>

The effect is simply to offset the coordinate system by <i>x</i> and <i>y</i>.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>