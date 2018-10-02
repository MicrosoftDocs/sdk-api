---
UID: NF:dcomp.IDCompositionTranslateTransform3D.SetOffsetY(IDCompositionAnimation)
title: IDCompositionTranslateTransform3D::SetOffsetY(IDCompositionAnimation)
author: windows-sdk-content
description: Changes the value of the OffsetY property of a 3D translation transform effect. The OffsetY property specifies the distance to translate along the y-axis.
old-location: directcomp\idcompositiontranslatetransform3d_setoffsety_float.htm
tech.root: directcomp
ms.assetid: 09A12F3B-84B8-43E5-A58E-61B43E5211FB
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDCompositionTranslateTransform3D interface [DirectComposition],SetOffsetY method, IDCompositionTranslateTransform3D.SetOffsetY, IDCompositionTranslateTransform3D.SetOffsetY(IDCompositionAnimation), IDCompositionTranslateTransform3D::SetOffsetY, IDCompositionTranslateTransform3D::SetOffsetY(IDCompositionAnimation), IDCompositionTranslateTransform3D::SetOffsetY(float), SetOffsetY, SetOffsetY method [DirectComposition], SetOffsetY method [DirectComposition],IDCompositionTranslateTransform3D interface, dcomp/IDCompositionTranslateTransform3D::SetOffsetY, directcomp.idcompositiontranslatetransform3d_setoffsety_float
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
 - IDCompositionTranslateTransform3D.SetOffsetY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionTranslateTransform3D::SetOffsetY(IDCompositionAnimation)


## -description


Changes the value of the OffsetY property of a 3D translation transform effect. The OffsetY property specifies the distance to translate along the y-axis.


## -parameters




### -param animation

TBD




#### - offsetY [in]

Type: <b>float</b>

The distance to translate along the y-axis, in pixels.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>offsetY</i> parameter is NaN, positive infinity, or negative infinity.



If the OffsetY property was previously animated, this method removes the animation and sets the OffsetY property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/C265E5FC-F7A1-4E87-8311-C4D0613DD7BC">IDCompositionTranslateTransform3D</a>



<a href="https://msdn.microsoft.com/61EDA0AA-0274-446E-9169-974AB84802FA">IDCompositionTranslateTransform3D::SetOffsetX</a>



<a href="https://msdn.microsoft.com/1467F8A8-15CF-4B3E-8816-76F2F5BFB68B">IDCompositionTranslateTransform3D::SetOffsetZ</a>
 

 

