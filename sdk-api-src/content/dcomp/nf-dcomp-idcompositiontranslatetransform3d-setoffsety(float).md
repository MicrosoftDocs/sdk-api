---
UID: NF:dcomp.IDCompositionTranslateTransform3D.SetOffsetY(float)
title: IDCompositionTranslateTransform3D::SetOffsetY (dcomp.h)
author: windows-sdk-content
description: Changes the value of the OffsetY property of a 3D translation transform effect. The OffsetY property specifies the distance to translate along the y-axis.
old-location: directcomp\idcompositiontranslatetransform3d_setoffsety_float.htm
tech.root: directcomp
ms.assetid: 09A12F3B-84B8-43E5-A58E-61B43E5211FB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionTranslateTransform3D interface [DirectComposition],SetOffsetY method, IDCompositionTranslateTransform3D.SetOffsetY, IDCompositionTranslateTransform3D::SetOffsetY, IDCompositionTranslateTransform3D::SetOffsetY(float), SetOffsetY, SetOffsetY method [DirectComposition], SetOffsetY method [DirectComposition],IDCompositionTranslateTransform3D interface, dcomp/IDCompositionTranslateTransform3D::SetOffsetY, directcomp.idcompositiontranslatetransform3d_setoffsety_float
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionTranslateTransform3D.SetOffsetY"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionTranslateTransform3D::SetOffsetY


## -description


Changes the value of the OffsetY property of a 3D translation transform effect. The OffsetY property specifies the distance to translate along the y-axis.


## -parameters




### -param offsetY [in]

Type: <b>float</b>

The distance to translate along the y-axis, in pixels.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>offsetY</i> parameter is NaN, positive infinity, or negative infinity.



If the OffsetY property was previously animated, this method removes the animation and sets the OffsetY property to the specified static value.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d">IDCompositionTranslateTransform3D</a>



<a href="https://docs.microsoft.com/windows/win32/api/dcomp/nf-dcomp-idcompositiontranslatetransform3d-setoffsetx(float)">IDCompositionTranslateTransform3D::SetOffsetX</a>



<a href="https://docs.microsoft.com/windows/win32/api/dcomp/nf-dcomp-idcompositiontranslatetransform3d-setoffsetz(float)">IDCompositionTranslateTransform3D::SetOffsetZ</a>
 

 

