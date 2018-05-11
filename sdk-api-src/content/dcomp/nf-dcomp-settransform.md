---
UID: NF:dcomp.SetTransform
title: SetTransform function
author: windows-driver-content
description: Sets the Transform property of this visual. The Transform property specifies a 3D transform used to modify the coordinate system of this visual. The property can specify either a 4-by-4 transform matrix or a transform object.
old-location: directcomp\idcompositionvisual3_settransform_overloaded.htm
old-project: directcomp
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IDCompositionVisual3::SetTransform, SetTransform, SetTransform methods [DirectComposition], dcomp/SetTransform, directcomp.idcompositionvisual3_settransform_overloaded
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: D2D_VECTOR_4F
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dcomp.dll
api_name:
-	IDCompositionVisual3::SetTransform
product: Windows
targetos: Windows
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# SetTransform function


## -description


<span>Sets the Transform property of this visual. The Transform  property specifies a 3D transform used to modify the coordinate system of this visual.
  The property can specify either a  4-by-4 transform matrix or a transform object.


</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1deb9c84-1a5b-5dac-af0f-ae6b49a9c473">SetTransform(D2D_MATRIX_4X4_F&)</a>
</td>
<td align="left" width="63%">
Sets the Transform property to the specified transform matrix.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04b20481-5d00-d8f9-290d-a8ab19ae6eba">SetTransform(IDCompositionTransform3D*)</a>
</td>
<td align="left" width="63%">
Sets the Transform property to the specified transformation object.

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://msdn.microsoft.com/150e33f2-3d76-44a8-b2fe-5a2b4a532c3c">IDCompositionMatrixTransform</a>



<a href="https://msdn.microsoft.com/6c92bd6b-4479-45c2-986c-0a6c91248361">IDCompositionRotateTransform</a>



<a href="https://msdn.microsoft.com/8e59c484-b7c5-446a-a5d6-e00371e2c08a">IDCompositionScaleTransform</a>



<a href="https://msdn.microsoft.com/c1dbc11f-b8e3-487e-84f0-517ebaf65de8">IDCompositionSkewTransform</a>



<a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a>



<a href="https://msdn.microsoft.com/2215721e-a10d-4c9e-b5b7-1698afa547d8">IDCompositionTranslateTransform</a>



<a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>



<a href="https://msdn.microsoft.com/c7bf4e6f-119b-2122-1103-d6ab240121c9">IDCompositionVisual3</a>



<a href="https://msdn.microsoft.com/0EFCDE12-3BF1-4D1F-8E28-54F3D7EEFFC1">IDCompositionVisual::SetOffsetX</a>



<a href="https://msdn.microsoft.com/E364BDB4-57E0-4206-9095-F39E6B5B9190">IDCompositionVisual::SetOffsetY</a>
 

 

