---
UID: NF:dcomp.IDCompositionRotateTransform.SetCenterY
title: IDCompositionRotateTransform::SetCenterY (dcomp.h)
author: windows-sdk-content
description: Changes the value of the CenterY property of a 2D rotation transform.
old-location: directcomp\idcompositionrotatetransform_setcentery_float.htm
tech.root: directcomp
ms.assetid: 7D4EF6C3-A0BA-42C4-841C-A40EEF5122F5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform interface [DirectComposition],SetCenterY method, IDCompositionRotateTransform.SetCenterY, IDCompositionRotateTransform::SetCenterY, IDCompositionRotateTransform::SetCenterY(float), SetCenterY, SetCenterY method [DirectComposition], SetCenterY method [DirectComposition],IDCompositionRotateTransform interface, dcomp/IDCompositionRotateTransform::SetCenterY, directcomp.idcompositionrotatetransform_setcentery_float
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
 - IDCompositionRotateTransform.SetCenterY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionRotateTransform::SetCenterY


## -description


Changes the value of the CenterY property of a 2D rotation transform. The CenterY property specifies the y-coordinate of the point about which the rotation is performed.


## -parameters




### -param centerY [in]

Type: <b>float</b>

The new y-coordinate of the center point.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>centerY</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterY property was previously animated, this method removes the animation and sets the CenterY property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/6c92bd6b-4479-45c2-986c-0a6c91248361">IDCompositionRotateTransform</a>



<a href="https://msdn.microsoft.com/D5CE4491-0A06-4824-BDE5-A839E0E60EA7">IDCompositionRotateTransform::SetCenterX</a>
 

 

