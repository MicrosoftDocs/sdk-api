---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetCenterY
title: IDCompositionRotateTransform3D::SetCenterY
author: windows-sdk-content
description: Changes the value of the CenterY property of a 3D rotation transform. The CenterY property specifies the y-coordinate of the point about which the rotation is performed. The default value is zero.
old-location: directcomp\idcompositionrotatetransform3d_setcentery_float.htm
tech.root: directcomp
ms.assetid: 3A7E562C-52ED-45A4-B473-6ACBF6A9C0E9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetCenterY method, IDCompositionRotateTransform3D.SetCenterY, IDCompositionRotateTransform3D::SetCenterY, IDCompositionRotateTransform3D::SetCenterY(float), SetCenterY, SetCenterY method [DirectComposition], SetCenterY method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetCenterY, directcomp.idcompositionrotatetransform3d_setcentery_float
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
 - IDCompositionRotateTransform3D.SetCenterY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionRotateTransform3D::SetCenterY


## -description


Changes the value of the CenterY property of a 3D rotation transform. The CenterY property specifies the y-coordinate of the point about which the rotation is performed. The default value is zero.


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




<a href="https://msdn.microsoft.com/BEC58B57-66A1-4645-A0B8-D546334E1E23">IDCompositionRotateTransform3D</a>



<a href="https://msdn.microsoft.com/D5CE4491-0A06-4824-BDE5-A839E0E60EA7">IDCompositionRotateTransform3D::SetCenterX</a>



<a href="https://msdn.microsoft.com/7FF293B6-8FAE-4277-8C07-EBD4E819E2A0">IDCompositionRotateTransform3D::SetCenterZ</a>
 

 

