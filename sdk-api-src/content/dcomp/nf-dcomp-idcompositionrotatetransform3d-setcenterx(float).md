---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetCenterX(float)
title: IDCompositionRotateTransform3D::SetCenterX(float)
author: windows-sdk-content
description: Changes the value of the CenterX property of a 3D rotation transform. The CenterX property specifies the x-coordinate of the point about which the rotation is performed. The default value is zero.
old-location: directcomp\idcompositionrotatetransform3d_setcenterx_float.htm
tech.root: directcomp
ms.assetid: 669A3002-23C0-44FA-ABC9-B4AE1C8A2C81
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetCenterX method, IDCompositionRotateTransform3D.SetCenterX, IDCompositionRotateTransform3D.SetCenterX(float), IDCompositionRotateTransform3D::SetCenterX, IDCompositionRotateTransform3D::SetCenterX(float), SetCenterX, SetCenterX method [DirectComposition], SetCenterX method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetCenterX, directcomp.idcompositionrotatetransform3d_setcenterx_float
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
 - IDCompositionRotateTransform3D.SetCenterX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionRotateTransform3D::SetCenterX(float)


## -description


Changes the value of the CenterX property of a 3D rotation transform. The CenterX property specifies the x-coordinate of the point about which the rotation is performed. The default value is zero.


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




<a href="https://msdn.microsoft.com/BEC58B57-66A1-4645-A0B8-D546334E1E23">IDCompositionRotateTransform3D</a>



<a href="https://msdn.microsoft.com/19B3B065-BE8C-4CBD-8A94-54934CA0B421">IDCompositionRotateTransform3D::SetCenterY</a>



<a href="https://msdn.microsoft.com/7FF293B6-8FAE-4277-8C07-EBD4E819E2A0">IDCompositionRotateTransform3D::SetCenterZ</a>
 

 

