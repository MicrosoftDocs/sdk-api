---
UID: NN:dcomp.IDCompositionMatrixTransform
title: IDCompositionMatrixTransform (dcomp.h)
author: windows-sdk-content
description: Represents an arbitrary affine 2D transformation defined by a 3-by-2 matrix.
old-location: directcomp\idcompositionmatrixtransform.htm
tech.root: directcomp
ms.assetid: 150e33f2-3d76-44a8-b2fe-5a2b4a532c3c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionMatrixTransform, IDCompositionMatrixTransform interface [DirectComposition], IDCompositionMatrixTransform interface [DirectComposition],described, dcomp/IDCompositionMatrixTransform, directcomp.idcompositionmatrixtransform
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
 - IDCompositionMatrixTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionMatrixTransform interface


## -description


Represents an arbitrary affine 2D transformation defined by a 3-by-2 matrix.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionMatrixTransform</b> interface inherits from <a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a>. <b>IDCompositionMatrixTransform</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1f164dfd-8bd4-4f6e-a5d2-d455808b5b0f">SetMatrix</a>
</td>
<td align="left" width="63%">
Changes all values of the matrix of this 2D transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ADF3D443-6764-40A5-AD5C-7C3053E247CB">SetMatrixElement</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of one element of the matrix of this 2D transform.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

