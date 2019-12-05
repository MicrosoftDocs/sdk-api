---
UID: NN:dcomp.IDCompositionMatrixTransform
title: IDCompositionMatrixTransform (dcomp.h)
description: Represents an arbitrary affine 2D transformation defined by a 3-by-2 matrix.
old-location: directcomp\idcompositionmatrixtransform.htm
tech.root: directcomp
ms.assetid: 150e33f2-3d76-44a8-b2fe-5a2b4a532c3c
ms.date: 12/05/2018
ms.keywords: IDCompositionMatrixTransform, IDCompositionMatrixTransform interface [DirectComposition], IDCompositionMatrixTransform interface [DirectComposition],described, dcomp/IDCompositionMatrixTransform, directcomp.idcompositionmatrixtransform
ms.topic: interface
f1_keywords:
- dcomp/IDCompositionMatrixTransform
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
- IDCompositionMatrixTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionMatrixTransform interface


## -description


Represents an arbitrary affine 2D transformation defined by a 3-by-2 matrix.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionMatrixTransform</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>. <b>IDCompositionMatrixTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionMatrixTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix">SetMatrix</a>
</td>
<td align="left" width="63%">
Changes all values of the matrix of this 2D transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437433(v=vs.85)">SetMatrixElement</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of one element of the matrix of this 2D transform.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
 

 

