---
UID: NF:dcomp.IDCompositionSkewTransform.SetAngleX(float)
title: IDCompositionSkewTransform::SetAngleX(float)
author: windows-sdk-content
description: Changes the value of the AngleX property of a 2D skew transform.
old-location: directcomp\idcompositionskewtransform_setanglex_float.htm
tech.root: directcomp
ms.assetid: FE38F14B-69EA-4129-A944-DBBF784B53DE
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDCompositionSkewTransform interface [DirectComposition],SetAngleX method, IDCompositionSkewTransform.SetAngleX, IDCompositionSkewTransform.SetAngleX(float), IDCompositionSkewTransform::SetAngleX, IDCompositionSkewTransform::SetAngleX(float), SetAngleX, SetAngleX method [DirectComposition], SetAngleX method [DirectComposition],IDCompositionSkewTransform interface, dcomp/IDCompositionSkewTransform::SetAngleX, directcomp.idcompositionskewtransform_setanglex_float
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
 - IDCompositionSkewTransform.SetAngleX
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
- IDCompositionSkewTransform.SetAngleX
: 
---

# IDCompositionSkewTransform::SetAngleX(float)


## -description


Changes the value of the AngleX property of a 2D skew transform.   The AngleX property specifies the skew angle along the x-axis.


## -parameters




### -param angleX [in]

Type: <b>float</b>

The new skew angle of the x-axis, in degrees. A positive value creates a counterclockwise skew, and a negative value creates a clockwise skew. For values less than –360 or greater than 360, the values wrap around and are treated as if the mathematical operation mod(360) was applied.


## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>angleX</i> parameter is NaN, positive infinity, or negative infinity.



If the AngleX property was previously animated, this method removes the animation and sets the AngleX property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/c1dbc11f-b8e3-487e-84f0-517ebaf65de8">IDCompositionSkewTransform</a>



<a href="https://msdn.microsoft.com/BD3D282C-5BBD-4BCE-AE15-4491A37D9149">IDCompositionSkewTransform::SetAngleY</a>
 

 

