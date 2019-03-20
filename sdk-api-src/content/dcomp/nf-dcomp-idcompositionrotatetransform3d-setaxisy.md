---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetAxisY
title: IDCompositionRotateTransform3D::SetAxisY (dcomp.h)
author: windows-sdk-content
description: Changes the value of the AxisY property of a 3D rotation transform. The AxisY property specifies the y-coordinate for the axis vector of rotation. The default value is zero.
old-location: directcomp\idcompositionrotatetransform3d_setaxisy_float.htm
tech.root: directcomp
ms.assetid: EEDED20E-B1AC-4464-ABB5-C413E10B3E7E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetAxisY method, IDCompositionRotateTransform3D.SetAxisY, IDCompositionRotateTransform3D::SetAxisY, IDCompositionRotateTransform3D::SetAxisY(float), SetAxisY, SetAxisY method [DirectComposition], SetAxisY method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetAxisY, directcomp.idcompositionrotatetransform3d_setaxisy_float
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
 - IDCompositionRotateTransform3D.SetAxisY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionRotateTransform3D::SetAxisY


## -description


Changes the value of the AxisY property of a 3D rotation transform. The AxisY property specifies the y-coordinate for the axis vector of rotation.  The default value is zero.


## -parameters




### -param axisY [in]

Type: <b>float</b>

The new y-coordinate for the axis vector of rotation. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



When setting the axis to a non-default value, you should always set all three axis properties (AxisX, AxisY, and AxisZ).

This method fails if the <i>axisY</i> parameter is NaN, positive infinity, or negative infinity.



If the AxisY property was previously animated, this method removes the animation and sets the AxisY property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/BEC58B57-66A1-4645-A0B8-D546334E1E23">IDCompositionRotateTransform3D</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh448939(v=VS.85).aspx">IDCompositionRotateTransform3D::SetAxisX</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh448951(v=VS.85).aspx">IDCompositionRotateTransform3D::SetAxisZ</a>
 

 

