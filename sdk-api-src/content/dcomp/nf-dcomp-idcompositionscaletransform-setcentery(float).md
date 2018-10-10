---
UID: NF:dcomp.IDCompositionScaleTransform.SetCenterY(float)
title: IDCompositionScaleTransform::SetCenterY(float)
author: windows-sdk-content
description: Changes the value of the CenterY property of a 2D scale transform.
old-location: directcomp\idcompositionscaletransform_setcentery_float.htm
tech.root: directcomp
ms.assetid: 32E8FCBD-75D8-4162-9388-57B0348BD46B
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IDCompositionScaleTransform interface [DirectComposition],SetCenterY method, IDCompositionScaleTransform.SetCenterY, IDCompositionScaleTransform.SetCenterY(float), IDCompositionScaleTransform::SetCenterY, IDCompositionScaleTransform::SetCenterY(float), SetCenterY, SetCenterY method [DirectComposition], SetCenterY method [DirectComposition],IDCompositionScaleTransform interface, dcomp/IDCompositionScaleTransform::SetCenterY, directcomp.idcompositionscaletransform_setcentery_float
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
 - IDCompositionScaleTransform.SetCenterY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionScaleTransform::SetCenterY(float)


## -description


Changes the value of the CenterY property of a 2D scale transform. The CenterY property specifies the y-coordinate of the point about which scaling is performed. 


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




<a href="https://msdn.microsoft.com/8e59c484-b7c5-446a-a5d6-e00371e2c08a">IDCompositionScaleTransform</a>



<a href="https://msdn.microsoft.com/5258F0D5-0034-4E02-8975-C5A530099727">IDCompositionScaleTransform::SetCenterX</a>
 

 

