---
UID: NF:dcomp.IDCompositionSkewTransform.SetAngleY
title: IDCompositionSkewTransform::SetAngleY
author: windows-sdk-content
description: Changes the value of the AngleY property of a 2D skew transform.
old-location: directcomp\idcompositionskewtransform_setangley_float.htm
tech.root: directcomp
ms.assetid: 5B356D5E-2F69-4620-880C-14F51786A8A5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionSkewTransform interface [DirectComposition],SetAngleY method, IDCompositionSkewTransform.SetAngleY, IDCompositionSkewTransform::SetAngleY, IDCompositionSkewTransform::SetAngleY(float), SetAngleY, SetAngleY method [DirectComposition], SetAngleY method [DirectComposition],IDCompositionSkewTransform interface, dcomp/IDCompositionSkewTransform::SetAngleY, directcomp.idcompositionskewtransform_setangley_float
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
 - IDCompositionSkewTransform.SetAngleY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionSkewTransform::SetAngleY


## -description


Changes the value of the AngleY property of a 2D skew transform. The AngleY property specifies the skew angle along the y-axis.


## -parameters




### -param angleY [in]

Type: <b>float</b>

The new skew angle of the y-axis, in degrees. A positive value creates a counterclockwise skew, and a negative value creates a clockwise skew. For values less than –360 or greater than 360, the values wrap around and are treated as if the mathematical operation mod(360) was applied.


## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>angleY</i> parameter is NaN, positive infinity, or negative infinity.



If the AngleY property was previously animated, this method removes the animation and sets the AngleY property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/c1dbc11f-b8e3-487e-84f0-517ebaf65de8">IDCompositionSkewTransform</a>



<a href="https://msdn.microsoft.com/DA4AEE0D-A913-434E-9150-DD6763132041">IDCompositionSkewTransform::SetAngleX</a>
 

 

