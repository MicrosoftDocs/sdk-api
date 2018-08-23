---
UID: NF:dcomp.IDCompositionScaleTransform.SetCenterX(IDCompositionAnimation)
title: IDCompositionScaleTransform::SetCenterX(IDCompositionAnimation)
author: windows-sdk-content
description: Changes the value of the CenterX property of a 2D scale transform.
old-location: directcomp\idcompositionscaletransform_setcenterx_float.htm
old-project: directcomp
ms.assetid: C2DA7251-AB71-400A-9016-04EB4A6F0B5D
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionScaleTransform interface [DirectComposition],SetCenterX method, IDCompositionScaleTransform.SetCenterX, IDCompositionScaleTransform.SetCenterX(IDCompositionAnimation), IDCompositionScaleTransform::SetCenterX, IDCompositionScaleTransform::SetCenterX(IDCompositionAnimation), IDCompositionScaleTransform::SetCenterX(float), SetCenterX, SetCenterX method [DirectComposition], SetCenterX method [DirectComposition],IDCompositionScaleTransform interface, dcomp/IDCompositionScaleTransform::SetCenterX, directcomp.idcompositionscaletransform_setcenterx_float
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
 - IDCompositionScaleTransform.SetCenterX
product: Windows
targetos: Windows
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# IDCompositionScaleTransform::SetCenterX(IDCompositionAnimation)


## -description


Changes the value of the CenterX property of a 2D scale transform.   The CenterX property specifies the x-coordinate of the point about which scaling is performed. 


## -parameters




### -param animation






#### - centerX [in]

Type: <b>float</b>

The new x-coordinate of the center point.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>centerX</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterX property was previously animated, this method removes the animation and sets the CenterX property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/8e59c484-b7c5-446a-a5d6-e00371e2c08a">IDCompositionScaleTransform</a>



<a href="https://msdn.microsoft.com/18A755E6-C6E8-437C-BBB5-58F36F754BE7">IDCompositionScaleTransform::SetCenterY</a>
 

 

