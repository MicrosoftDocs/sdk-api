---
UID: NF:dcomp.IDCompositionSkewTransform.SetCenterY(float)
title: IDCompositionSkewTransform::SetCenterY(float)
author: windows-sdk-content
description: Changes the value of the CenterY property of a 2D skew transform.
old-location: directcomp\idcompositionskewtransform_setcentery_float.htm
tech.root: directcomp
ms.assetid: A67FEAC7-1EBA-42D2-A917-4D5DEA71F557
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDCompositionSkewTransform interface [DirectComposition],SetCenterY method, IDCompositionSkewTransform.SetCenterY, IDCompositionSkewTransform.SetCenterY(float), IDCompositionSkewTransform::SetCenterY, IDCompositionSkewTransform::SetCenterY(float), SetCenterY, SetCenterY method [DirectComposition], SetCenterY method [DirectComposition],IDCompositionSkewTransform interface, dcomp/IDCompositionSkewTransform::SetCenterY, directcomp.idcompositionskewtransform_setcentery_float
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
 - IDCompositionSkewTransform.SetCenterY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dcomp.h
: 
- IDCompositionSkewTransform.SetCenterY
: 
---

# IDCompositionSkewTransform::SetCenterY(float)


## -description


Changes the value of the CenterY property of a 2D skew transform. The CenterY property specifies the y-coordinate of the point about which the skew is performed.


## -parameters




### -param centerY [in]

Type: <b>float</b>

The new y-coordinate of the center point.


## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>centerY</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterY property was previously animated, this method removes the animation and sets the CenterY property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/c1dbc11f-b8e3-487e-84f0-517ebaf65de8">IDCompositionSkewTransform</a>



<a href="https://msdn.microsoft.com/934E3D60-45F4-4645-8E77-22F7E4AEAD60">IDCompositionSkewTransform::SetCenterX</a>
 

 

