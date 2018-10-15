---
UID: NF:dcomp.IDCompositionScaleTransform3D.SetScaleX(IDCompositionAnimation)
title: IDCompositionScaleTransform3D::SetScaleX(IDCompositionAnimation)
author: windows-sdk-content
description: Changes the value of the ScaleX property of a 3D scale transform.
old-location: directcomp\idcompositionscaletransform3d_setscalex_float.htm
tech.root: directcomp
ms.assetid: 6461C857-AC6E-4F27-9DE2-F1B3E00846D8
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IDCompositionScaleTransform3D interface [DirectComposition],SetScaleX method, IDCompositionScaleTransform3D.SetScaleX, IDCompositionScaleTransform3D.SetScaleX(IDCompositionAnimation), IDCompositionScaleTransform3D::SetScaleX, IDCompositionScaleTransform3D::SetScaleX(IDCompositionAnimation), IDCompositionScaleTransform3D::SetScaleX(float), SetScaleX, SetScaleX method [DirectComposition], SetScaleX method [DirectComposition],IDCompositionScaleTransform3D interface, dcomp/IDCompositionScaleTransform3D::SetScaleX, directcomp.idcompositionscaletransform3d_setscalex_float
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
 - IDCompositionScaleTransform3D.SetScaleX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionScaleTransform3D::SetScaleX(IDCompositionAnimation)


## -description


Changes the value of the ScaleX property of a 3D scale transform. The ScaleX property specifies the scale factor along the x-axis.


## -parameters




### -param animation

TBD




#### - scaleX [in]

Type: <b>float</b>

The new x-axis scale factor.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>scaleX</i> parameter is NaN, positive infinity, or negative infinity.



If the ScaleX property was previously animated, this method removes the animation and sets the ScaleX property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/8e59c484-b7c5-446a-a5d6-e00371e2c08a">IDCompositionScaleTransform3D</a>



<a href="https://msdn.microsoft.com/90E48F55-B9A3-464D-9FB2-03AA27AA5A08">IDCompositionScaleTransform3D::SetScaleY</a>



<a href="https://msdn.microsoft.com/CD00FBB3-246E-45D0-A7F6-5A7F9C37376B">IDCompositionScaleTransform3D::SetScaleZ</a>
 

 

