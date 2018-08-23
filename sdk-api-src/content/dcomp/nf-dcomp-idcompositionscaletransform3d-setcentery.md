---
UID: NF:dcomp.IDCompositionScaleTransform3D.SetCenterY
title: IDCompositionScaleTransform3D::SetCenterY
author: windows-sdk-content
description: Changes the value of the CenterY property of a 3D scale transform.
old-location: directcomp\idcompositionscaletransform3d_setcentery_float.htm
old-project: directcomp
ms.assetid: A50A8309-08F7-4868-AB95-A825C60C7E9E
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionScaleTransform3D interface [DirectComposition],SetCenterY method, IDCompositionScaleTransform3D.SetCenterY, IDCompositionScaleTransform3D::SetCenterY, IDCompositionScaleTransform3D::SetCenterY(float), SetCenterY, SetCenterY method [DirectComposition], SetCenterY method [DirectComposition],IDCompositionScaleTransform3D interface, dcomp/IDCompositionScaleTransform3D::SetCenterY, directcomp.idcompositionscaletransform3d_setcentery_float
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D_VECTOR_4F
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionScaleTransform3D.SetCenterY
product: Windows
targetos: Windows
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# IDCompositionScaleTransform3D::SetCenterY


## -description


Changes the value of the CenterY property of a 3D scale transform.   The CenterY property specifies the y-coordinate of the point about which scaling is performed. 


## -parameters




#### - centerY [in]

Type: <b>float</b>

The new y-coordinate of the center point.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>centerY</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterY property was previously animated, this method removes the animation and sets the CenterY property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/8e59c484-b7c5-446a-a5d6-e00371e2c08a">IDCompositionScaleTransform3D</a>



<a href="https://msdn.microsoft.com/959F8530-D2D5-46BC-9F29-F1DFC8029C12">IDCompositionScaleTransform3D::SetCenterX</a>



<a href="https://msdn.microsoft.com/1A5C63FE-2378-4274-8ADD-04A88B60FF8F">IDCompositionScaleTransform3D::SetCenterZ</a>
 

 

