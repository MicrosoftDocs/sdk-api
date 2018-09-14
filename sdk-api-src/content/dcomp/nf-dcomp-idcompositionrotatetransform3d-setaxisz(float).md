---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetAxisZ(float)
title: IDCompositionRotateTransform3D::SetAxisZ(float)
author: windows-sdk-content
description: Changes the value of the AxisZ property of a 3D rotation transform. The AxisZ property specifies the z-coordinate for the axis vector of rotation. The default value is 1.0.
old-location: directcomp\idcompositionrotatetransform3d_setaxisz_float.htm
tech.root: directcomp
ms.assetid: 2150E564-0E19-40E9-9D33-53EA17917A8F
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetAxisZ method, IDCompositionRotateTransform3D.SetAxisZ, IDCompositionRotateTransform3D.SetAxisZ(float), IDCompositionRotateTransform3D::SetAxisZ, IDCompositionRotateTransform3D::SetAxisZ(float), SetAxisZ, SetAxisZ method [DirectComposition], SetAxisZ method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetAxisZ, directcomp.idcompositionrotatetransform3d_setaxisz_float
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
 - IDCompositionRotateTransform3D.SetAxisZ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionRotateTransform3D::SetAxisZ(float)


## -description


Changes the value of the AxisZ property of a 3D rotation transform. The AxisZ property specifies the z-coordinate for the axis vector of rotation. The default value is 1.0.


## -parameters




### -param axisZ [in]

Type: <b>float</b>

The new z-coordinate for the axis vector of rotation. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



When setting the axis to a non-default value, you should always set all three axis properties (AxisX, AxisY, and AxisZ).

This method fails if the <i>axisZ</i> parameter is NaN, positive infinity, or negative infinity.



If the AxisZ property was previously animated, this method removes the animation and sets the AxisX property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/BEC58B57-66A1-4645-A0B8-D546334E1E23">IDCompositionRotateTransform3D</a>



<a href="https://msdn.microsoft.com/6ADBB027-8F80-4DF3-9199-DDB6570DF81B">IDCompositionRotateTransform3D::SetAxisX</a>



<a href="https://msdn.microsoft.com/C86E4D59-4E9D-44BF-BA9D-91714D0C2D37">IDCompositionRotateTransform3D::SetAxisY</a>
 

 

