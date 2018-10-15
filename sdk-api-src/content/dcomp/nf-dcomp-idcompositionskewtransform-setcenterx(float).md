---
UID: NF:dcomp.IDCompositionSkewTransform.SetCenterX(float)
title: IDCompositionSkewTransform::SetCenterX(float)
author: windows-sdk-content
description: Changes the value of the CenterX property of a 2D skew transform.
old-location: directcomp\idcompositionskewtransform_setcenterx_float.htm
tech.root: directcomp
ms.assetid: 706A9DDF-ED32-4694-9FF6-580F7AFAB09F
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IDCompositionSkewTransform interface [DirectComposition],SetCenterX method, IDCompositionSkewTransform.SetCenterX, IDCompositionSkewTransform.SetCenterX(float), IDCompositionSkewTransform::SetCenterX, IDCompositionSkewTransform::SetCenterX(float), SetCenterX, SetCenterX method [DirectComposition], SetCenterX method [DirectComposition],IDCompositionSkewTransform interface, dcomp/IDCompositionSkewTransform::SetCenterX, directcomp.idcompositionskewtransform_setcenterx_float
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
 - IDCompositionSkewTransform.SetCenterX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionSkewTransform::SetCenterX(float)


## -description


Changes the value of the CenterX property of a 2D skew transform. The CenterX property specifies the x-coordinate of the point about which the skew is performed.


## -parameters




### -param centerX [in]

Type: <b>float</b>

The new x-coordinate of the center point.


## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>centerX</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterX property was previously animated, this method removes the animation and sets the CenterX property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/c1dbc11f-b8e3-487e-84f0-517ebaf65de8">IDCompositionSkewTransform</a>



<a href="https://msdn.microsoft.com/D3F5E009-D6D2-431F-AC5C-C14C0AE1CD36">IDCompositionSkewTransform::SetCenterY</a>
 

 

