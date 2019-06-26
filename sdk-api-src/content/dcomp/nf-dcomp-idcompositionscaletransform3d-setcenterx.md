---
UID: NF:dcomp.IDCompositionScaleTransform3D.SetCenterX
title: IDCompositionScaleTransform3D::SetCenterX (dcomp.h)
author: windows-sdk-content
description: Changes the value of the CenterX property of a 3D scale transform.
old-location: directcomp\idcompositionscaletransform3d_setcenterx_float.htm
tech.root: directcomp
ms.assetid: 4AB99A66-BB3B-4AA5-B041-3F4F77AF93CE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionScaleTransform3D interface [DirectComposition],SetCenterX method, IDCompositionScaleTransform3D.SetCenterX, IDCompositionScaleTransform3D::SetCenterX, IDCompositionScaleTransform3D::SetCenterX(float), SetCenterX, SetCenterX method [DirectComposition], SetCenterX method [DirectComposition],IDCompositionScaleTransform3D interface, dcomp/IDCompositionScaleTransform3D::SetCenterX, directcomp.idcompositionscaletransform3d_setcenterx_float
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionScaleTransform3D.SetCenterX"
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
 - IDCompositionScaleTransform3D.SetCenterX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionScaleTransform3D::SetCenterX


## -description


Changes the value of the CenterX property of a 3D scale transform.   The CenterX property specifies the x-coordinate of the point about which scaling is performed. 


## -parameters




### -param centerX [in]

Type: <b>float</b>

The new x-coordinate of the center point.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>centerX</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterX property was previously animated, this method removes the animation and sets the CenterX property to the specified static value.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform">IDCompositionScaleTransform3D</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449006(v=vs.85)">IDCompositionScaleTransform3D::SetCenterY</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449012(v=vs.85)">IDCompositionScaleTransform3D::SetCenterZ</a>
 

 

