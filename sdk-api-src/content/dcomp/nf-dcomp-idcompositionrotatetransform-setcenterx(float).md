---
UID: NF:dcomp.IDCompositionRotateTransform.SetCenterX(float)
title: IDCompositionRotateTransform::SetCenterX(float)
author: windows-sdk-content
description: Changes the value of the CenterX property of a 2D rotation transform.
old-location: directcomp\idcompositionrotatetransform_setcenterx_float.htm
tech.root: directcomp
ms.assetid: A1E2E033-031E-4781-9FCC-DC3190CCAB61
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IDCompositionRotateTransform interface [DirectComposition],SetCenterX method, IDCompositionRotateTransform.SetCenterX, IDCompositionRotateTransform.SetCenterX(float), IDCompositionRotateTransform::SetCenterX, IDCompositionRotateTransform::SetCenterX(float), SetCenterX, SetCenterX method [DirectComposition], SetCenterX method [DirectComposition],IDCompositionRotateTransform interface, dcomp/IDCompositionRotateTransform::SetCenterX, directcomp.idcompositionrotatetransform_setcenterx_float
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
 - IDCompositionRotateTransform.SetCenterX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionRotateTransform::SetCenterX(float)


## -description


Changes the value of the CenterX property of a 2D rotation transform. The CenterX property specifies the x-coordinate of the point about which the rotation is performed.


## -parameters




### -param centerX [in]

Type: <b>float</b>

The new x-coordinate of the center point.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>centerX</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterX property was previously animated, this method removes the animation and sets the CenterX property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/6c92bd6b-4479-45c2-986c-0a6c91248361">IDCompositionRotateTransform</a>



<a href="https://msdn.microsoft.com/4C586C46-AA3E-4572-AFD6-8661BD26AC50">IDCompositionRotateTransform::SetCenterY</a>
 

 

