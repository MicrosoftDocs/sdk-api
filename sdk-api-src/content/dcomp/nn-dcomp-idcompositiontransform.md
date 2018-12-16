---
UID: NN:dcomp.IDCompositionTransform
title: IDCompositionTransform
author: windows-sdk-content
description: Represents a 2D transformation that can be used to modify the coordinate space of a visual subtree.
old-location: directcomp\idcompositiontransform.htm
tech.root: directcomp
ms.assetid: 22f0d199-5162-4869-909e-d0ed0059b773
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionTransform, IDCompositionTransform interface [DirectComposition], IDCompositionTransform interface [DirectComposition],described, dcomp/IDCompositionTransform, directcomp.idcompositiontransform
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
 - IDCompositionTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionTransform interface


## -description


Represents a 2D transformation that can be used to modify the coordinate space of a visual subtree. 


## -remarks



The <b>IDCompositionTransform</b> interface is an abstract interface that represents a 2D affine transformation. Transformations affect the entire visual subtree that is rooted at the visual that the transform is associated with. A transform object can be associated with multiple visuals. When a transform object is modified, all affected visuals are recomposed to reflect the change.

Transforms operate by modifying the coordinate system for all rendering operations on a visual. For example, ordinarily a bitmap that is associated with a visual draws at position (0,0) and extends the full width and height of the bitmap. If a translation transform is applied, the bitmap draws at a position that is offset by that transform. If a scale transform is applied, the extent covered by the bitmap is affected by the scale transform. More than one transform can be simultaneously applied to a visual by using the <a href="https://msdn.microsoft.com/en-us/library/Hh437410(v=VS.85).aspx">IDCompositionDevice::CreateTransformGroup</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

