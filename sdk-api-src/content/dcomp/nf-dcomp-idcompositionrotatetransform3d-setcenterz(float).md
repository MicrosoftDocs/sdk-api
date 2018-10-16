---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetCenterZ(float)
title: IDCompositionRotateTransform3D::SetCenterZ(float)
author: windows-sdk-content
description: Changes the value of the CenterZ property of a 3D rotation transform. The CenterZ property specifies the z-coordinate of the point about which the rotation is performed. The default value is zero.
old-location: directcomp\idcompositionrotatetransform3d_setcenterz_float.htm
tech.root: directcomp
ms.assetid: 56406AD4-F257-444C-8E72-6B9A901D6075
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetCenterZ method, IDCompositionRotateTransform3D.SetCenterZ, IDCompositionRotateTransform3D.SetCenterZ(float), IDCompositionRotateTransform3D::SetCenterZ, IDCompositionRotateTransform3D::SetCenterZ(float), SetCenterZ, SetCenterZ method [DirectComposition], SetCenterZ method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetCenterZ, directcomp.idcompositionrotatetransform3d_setcenterz_float
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
 - IDCompositionRotateTransform3D.SetCenterZ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionRotateTransform3D::SetCenterZ(float)


## -description


Changes the value of the CenterZ property of a 3D rotation transform. The CenterZ property specifies the z-coordinate of the point about which the rotation is performed. The default value is zero.


## -parameters




### -param centerZ [in]

Type: <b>float</b>

The new z-coordinate of the center point.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>centerZ</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterZ property was previously animated, this method removes the animation and sets the CenterZ property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/BEC58B57-66A1-4645-A0B8-D546334E1E23">IDCompositionRotateTransform3D</a>



<a href="https://msdn.microsoft.com/2E4924A5-64D0-4415-B345-0DE9A0900258">IDCompositionRotateTransform3D::SetCenterX</a>



<a href="https://msdn.microsoft.com/19B3B065-BE8C-4CBD-8A94-54934CA0B421">IDCompositionRotateTransform3D::SetCenterY</a>
 

 

