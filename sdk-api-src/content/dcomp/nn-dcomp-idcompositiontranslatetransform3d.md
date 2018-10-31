---
UID: NN:dcomp.IDCompositionTranslateTransform3D
title: IDCompositionTranslateTransform3D
author: windows-sdk-content
description: Represents a 3D transformation that affects the offset of a visual along the x-axis, y-axis, and z-axis.
old-location: directcomp\idcompositiontranslatetransform3d.htm
tech.root: directcomp
ms.assetid: C265E5FC-F7A1-4E87-8311-C4D0613DD7BC
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDCompositionTranslateTransform3D, IDCompositionTranslateTransform3D interface [DirectComposition], IDCompositionTranslateTransform3D interface [DirectComposition],described, dcomp/IDCompositionTranslateTransform3D, directcomp.idcompositiontranslatetransform3d
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
 - IDCompositionTranslateTransform3D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionTranslateTransform3D interface


## -description


Represents a 3D transformation that affects the offset of a visual along the x-axis, y-axis, and z-axis. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionTranslateTransform3D</b> interface inherits from <a href="https://msdn.microsoft.com/81239AB4-C2A3-4E37-95E3-B3C10532EE15">IDCompositionTransform3D</a>. <b>IDCompositionTranslateTransform3D</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionTranslateTransform3D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61EDA0AA-0274-446E-9169-974AB84802FA">SetOffsetX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the OffsetX property of a 3D translation transform effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/254DCA74-DB51-442D-9483-F7597643C538">SetOffsetY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the OffsetY property of a 3D translation transform effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1467F8A8-15CF-4B3E-8816-76F2F5BFB68B">SetOffsetZ</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the OffsetZ property of a 3D translation transform effect.

</td>
</tr>
</table> 


## -remarks



A 3D translation transform represents the following 4-by-4 matrix:
      

<img alt="Four-by-four translation matrix" src="images/3D_translate_transform_4x4matrix.png"/>

The effect is to offset the blending position of the visual's subtree by <i>x</i>, <i>y</i>, and <i>z</i>.




## -see-also




<a href="https://msdn.microsoft.com/40935581-D45C-496B-90B9-152963F0B55A">IDCompositionEffectGroup::SetTransform3D</a>



<a href="https://msdn.microsoft.com/81239AB4-C2A3-4E37-95E3-B3C10532EE15">IDCompositionTransform3D</a>



<a href="https://msdn.microsoft.com/CCA785F6-869C-460A-AF54-573BDE798685">IDCompositionVisual::SetEffect</a>
 

 

