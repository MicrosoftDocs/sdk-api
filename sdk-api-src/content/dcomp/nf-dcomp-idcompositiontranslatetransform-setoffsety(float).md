---
UID: NF:dcomp.IDCompositionTranslateTransform.SetOffsetY(float)
title: IDCompositionTranslateTransform::SetOffsetY(float)
author: windows-sdk-content
description: Changes the value of the OffsetY property of a 2D translation transform.
old-location: directcomp\idcompositiontranslatetransform_setoffsety_float.htm
tech.root: directcomp
ms.assetid: 7EF80FFC-FB9B-4F4D-A321-7871E6C2E757
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDCompositionTranslateTransform interface [DirectComposition],SetOffsetY method, IDCompositionTranslateTransform.SetOffsetY, IDCompositionTranslateTransform.SetOffsetY(float), IDCompositionTranslateTransform::SetOffsetY, IDCompositionTranslateTransform::SetOffsetY(float), SetOffsetY, SetOffsetY method [DirectComposition], SetOffsetY method [DirectComposition],IDCompositionTranslateTransform interface, dcomp/IDCompositionTranslateTransform::SetOffsetY, directcomp.idcompositiontranslatetransform_setoffsety_float
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
 - IDCompositionTranslateTransform.SetOffsetY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionTranslateTransform::SetOffsetY(float)


## -description


Changes the value of the OffsetY property of a 2D translation transform. The OffsetY property specifies the distance to translate along the y-axis.


## -parameters




### -param offsetY [in]

Type: <b>float</b>

The distance to translate along the y-axis, in pixels.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>offsetY</i> parameter is NaN, positive infinity, or negative infinity.



If the OffsetY property was previously animated, this method removes the animation and sets the OffsetY property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/2215721e-a10d-4c9e-b5b7-1698afa547d8">IDCompositionTranslateTransform</a>



<a href="https://msdn.microsoft.com/E77645DB-6C6F-4A6C-9BD1-F2CF5915A85E">IDCompositionTranslateTransform::SetOffsetX</a>
 

 

