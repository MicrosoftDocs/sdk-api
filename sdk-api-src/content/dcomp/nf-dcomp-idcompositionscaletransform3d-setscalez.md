---
UID: NF:dcomp.IDCompositionScaleTransform3D.SetScaleZ
title: IDCompositionScaleTransform3D::SetScaleZ (dcomp.h)
author: windows-sdk-content
description: Changes the value of the ScaleZ property of a 3D scale transform.
old-location: directcomp\idcompositionscaletransform3d_setscalez_float.htm
tech.root: directcomp
ms.assetid: 9238ACAD-C6A6-4804-BF12-B28A498C03A9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionScaleTransform3D interface [DirectComposition],SetScaleZ method, IDCompositionScaleTransform3D.SetScaleZ, IDCompositionScaleTransform3D::SetScaleZ, IDCompositionScaleTransform3D::SetScaleZ(float), SetScaleZ, SetScaleZ method [DirectComposition], SetScaleZ method [DirectComposition],IDCompositionScaleTransform3D interface, dcomp/IDCompositionScaleTransform3D::SetScaleZ, directcomp.idcompositionscaletransform3d_setscalez_float
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
 - IDCompositionScaleTransform3D.SetScaleZ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionScaleTransform3D::SetScaleZ


## -description


Changes the value of the ScaleZ property of a 3D scale transform. The ScaleZ property specifies the scale factor along the z-axis.


## -parameters




### -param scaleZ [in]

Type: <b>float</b>

The new z-axis scale factor.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>scaleZ</i> parameter is NaN, positive infinity, or negative infinity.



If the ScaleZ property was previously animated, this method removes the animation and sets the ScaleZ property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/8e59c484-b7c5-446a-a5d6-e00371e2c08a">IDCompositionScaleTransform3D</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449018(v=VS.85).aspx">IDCompositionScaleTransform3D::SetScaleX</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449024(v=VS.85).aspx">IDCompositionScaleTransform3D::SetScaleY</a>
 

 

