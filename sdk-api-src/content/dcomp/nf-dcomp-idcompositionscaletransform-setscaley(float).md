---
UID: NF:dcomp.IDCompositionScaleTransform.SetScaleY(float)
title: IDCompositionScaleTransform::SetScaleY(float)
author: windows-sdk-content
description: Changes the value of the ScaleY property of a 2D scale transform.
old-location: directcomp\idcompositionscaletransform_setscaley_float.htm
tech.root: directcomp
ms.assetid: D47D6FA3-D5D2-47BD-8DE0-6E0EE08EE7C4
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IDCompositionScaleTransform interface [DirectComposition],SetScaleY method, IDCompositionScaleTransform.SetScaleY, IDCompositionScaleTransform.SetScaleY(float), IDCompositionScaleTransform::SetScaleY, IDCompositionScaleTransform::SetScaleY(float), SetScaleY, SetScaleY method [DirectComposition], SetScaleY method [DirectComposition],IDCompositionScaleTransform interface, dcomp/IDCompositionScaleTransform::SetScaleY, directcomp.idcompositionscaletransform_setscaley_float
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
 - IDCompositionScaleTransform.SetScaleY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionScaleTransform::SetScaleY(float)


## -description


Changes the value of the ScaleY property of a 2D scale transform. The ScaleY property specifies the scale factor along the y-axis.


## -parameters




### -param scaleY [in]

Type: <b>float</b>

The new y-axis scale factor.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>scaleY</i> parameter is NaN, positive infinity, or negative infinity.



If the ScaleY property was previously animated, this method removes the animation and sets the ScaleY property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/8e59c484-b7c5-446a-a5d6-e00371e2c08a">IDCompositionScaleTransform</a>



<a href="https://msdn.microsoft.com/114C4907-280C-4060-9157-30E0E8989251">IDCompositionScaleTransform::SetScaleX</a>
 

 

