---
UID: NF:dcomp.IDCompositionTranslateTransform.SetOffsetX(IDCompositionAnimation)
title: IDCompositionTranslateTransform::SetOffsetX(IDCompositionAnimation)
author: windows-sdk-content
description: Changes the value of the OffsetX property of a 2D translation transform.
old-location: directcomp\idcompositiontranslatetransform_setoffsetx_float.htm
tech.root: directcomp
ms.assetid: F5D96E02-2FB0-45AD-8F4A-8FB955A40C3F
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IDCompositionTranslateTransform interface [DirectComposition],SetOffsetX method, IDCompositionTranslateTransform.SetOffsetX, IDCompositionTranslateTransform.SetOffsetX(IDCompositionAnimation), IDCompositionTranslateTransform::SetOffsetX, IDCompositionTranslateTransform::SetOffsetX(IDCompositionAnimation), IDCompositionTranslateTransform::SetOffsetX(float), SetOffsetX, SetOffsetX method [DirectComposition], SetOffsetX method [DirectComposition],IDCompositionTranslateTransform interface, dcomp/IDCompositionTranslateTransform::SetOffsetX, directcomp.idcompositiontranslatetransform_setoffsetx_float
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDCompositionTranslateTransform.SetOffsetX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionTranslateTransform::SetOffsetX(IDCompositionAnimation)


## -description


Changes the value of the OffsetX property of a 2D translation transform. The OffsetX property specifies the distance to translate along the x-axis.


## -parameters




### -param animation

TBD




#### - offsetX [in]

Type: <b>float</b>

 The distance to translate along the x-axis, in pixels.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method perfoms an affine transformation, which moves every point by a fixed distance in the same direction. It is similar to shifting the origin of the coordinate space. 

This method fails if the <i>offsetX</i> parameter is NaN, positive infinity, or negative infinity.



If the OffsetX property was previously animated, this method removes the animation and sets the OffsetX property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/2215721e-a10d-4c9e-b5b7-1698afa547d8">IDCompositionTranslateTransform</a>



<a href="https://msdn.microsoft.com/D3E750A9-4890-4E4A-A5EE-2FF4CF9A9E62">IDCompositionTranslateTransform::SetOffsetY</a>
 

 

