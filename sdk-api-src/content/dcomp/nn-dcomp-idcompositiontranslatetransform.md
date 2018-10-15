---
UID: NN:dcomp.IDCompositionTranslateTransform
title: IDCompositionTranslateTransform
author: windows-sdk-content
description: Represents a 2D transformation that affects only the offset of a visual along the x-axis and y-axis.
old-location: directcomp\idcompositiontranslatetransform.htm
tech.root: directcomp
ms.assetid: 2215721e-a10d-4c9e-b5b7-1698afa547d8
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IDCompositionTranslateTransform, IDCompositionTranslateTransform interface [DirectComposition], IDCompositionTranslateTransform interface [DirectComposition],described, dcomp/IDCompositionTranslateTransform, directcomp.idcompositiontranslatetransform
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
 - IDCompositionTranslateTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionTranslateTransform interface


## -description


Represents a 2D transformation that affects only the offset of a visual along the x-axis and y-axis.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionTranslateTransform</b> interface inherits from <a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a>. <b>IDCompositionTranslateTransform</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/E77645DB-6C6F-4A6C-9BD1-F2CF5915A85E">SetOffsetX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the OffsetX property of a 2D translation transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D3E750A9-4890-4E4A-A5EE-2FF4CF9A9E62">SetOffsetY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the OffsetY property of a 2D translation transform.

</td>
</tr>
</table> 


## -remarks



A translation transform represents the following 3-by-2 matrix:

<img alt="Three-by-two translation matrix" src="images/translate_transform_3x2matrix.png"/>

The effect is simply to offset the coordinate system by <i>x</i> and <i>y</i>.




## -see-also




<a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

