---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetAxisX(IDCompositionAnimation)
title: IDCompositionRotateTransform3D::SetAxisX(IDCompositionAnimation)
author: windows-sdk-content
description: Animates the value of the AxisX property of a 3D rotation transform. The AxisX property specifies the x-coordinate for the axis vector of rotation. The default value is zero.
old-location: directcomp\idcompositionrotatetransform3d_setaxisx_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: EC871F31-BFBC-4AF6-9A1C-BD4EBBBCD6C3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetAxisX method, IDCompositionRotateTransform3D.SetAxisX, IDCompositionRotateTransform3D.SetAxisX(IDCompositionAnimation), IDCompositionRotateTransform3D::SetAxisX, IDCompositionRotateTransform3D::SetAxisX(IDCompositionAnimation), IDCompositionRotateTransform3D::SetAxisX(IDCompositionAnimation*), SetAxisX, SetAxisX method [DirectComposition], SetAxisX method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetAxisX, directcomp.idcompositionrotatetransform3d_setaxisx_idcompositionanimation
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
 - IDCompositionRotateTransform3D.SetAxisX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionRotateTransform3D::SetAxisX(IDCompositionAnimation)


## -description


Animates the value of the AxisX property of a 3D rotation transform. The AxisX property specifies the x-coordinate for the axis vector of rotation. The default value is zero.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the AxisX property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



When setting the axis to a non-default value, you should always set all three axis properties (AxisX, AxisY, and AxisZ).

This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the AxisX property unless this method is called again. If the AxisX property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/en-us/library/Hh437392(v=VS.85).aspx">IDCompositionDevice</a> interface as the affected 3D transform. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh448927(v=VS.85).aspx">IDCompositionRotateTransform3D</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh448945(v=VS.85).aspx">IDCompositionRotateTransform3D::SetAxisY</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh448951(v=VS.85).aspx">IDCompositionRotateTransform3D::SetAxisZ</a>
 

 

