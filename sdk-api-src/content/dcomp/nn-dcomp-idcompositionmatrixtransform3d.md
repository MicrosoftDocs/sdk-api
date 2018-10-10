---
UID: NN:dcomp.IDCompositionMatrixTransform3D
title: IDCompositionMatrixTransform3D
author: windows-sdk-content
description: Represents an arbitrary 3D transformation defined by a 4-by-4 matrix.
old-location: directcomp\idcompositionmatrixtransform3d.htm
tech.root: directcomp
ms.assetid: 56C9A564-2504-4940-B850-D280C8E0CF82
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IDCompositionMatrixTransform3D, IDCompositionMatrixTransform3D interface [DirectComposition], IDCompositionMatrixTransform3D interface [DirectComposition],described, dcomp/IDCompositionMatrixTransform3D, directcomp.idcompositionmatrixtransform3d
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
 - IDCompositionMatrixTransform3D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionMatrixTransform3D interface


## -description


Represents an arbitrary 3D transformation defined by a 4-by-4 matrix.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionMatrixTransform3D</b> interface inherits from <a href="https://msdn.microsoft.com/81239AB4-C2A3-4E37-95E3-B3C10532EE15">IDCompositionTransform3D</a>. <b>IDCompositionMatrixTransform3D</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionMatrixTransform3D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0F1DBC1C-154A-4785-B9B9-924353FD5836">SetMatrix</a>
</td>
<td align="left" width="63%">
Changes all values of the matrix of this 3D transformation effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0494B335-B613-4F0A-9CDA-3BBC63A7B996">SetMatrixElement</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of one element of the matrix of this 3D transform.

</td>
</tr>
</table> 


## -remarks



A 3D matrix transform represents the following 4-by-4 matrix:

<img alt="Four-by-four 3D transform matrix" src="images/3D_matrix.png"/>

 The application can set any of the values in the first three columns. Note that the fourth column is padded to allow for matrix concatenation. 




## -see-also




<a href="https://msdn.microsoft.com/81239AB4-C2A3-4E37-95E3-B3C10532EE15">IDCompositionTransform3D</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

