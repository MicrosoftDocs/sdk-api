---
UID: NF:dcomp.IDCompositionScaleTransform.SetScaleY(float)
title: IDCompositionScaleTransform::SetScaleY (dcomp.h)
description: Changes the value of the ScaleY property of a 2D scale transform.
helpviewer_keywords: ["IDCompositionScaleTransform interface [DirectComposition]","SetScaleY method","IDCompositionScaleTransform.SetScaleY","IDCompositionScaleTransform::SetScaleY","IDCompositionScaleTransform::SetScaleY(float)","SetScaleY","SetScaleY method [DirectComposition]","SetScaleY method [DirectComposition]","IDCompositionScaleTransform interface","dcomp/IDCompositionScaleTransform::SetScaleY","directcomp.idcompositionscaletransform_setscaley_float"]
old-location: directcomp\idcompositionscaletransform_setscaley_float.htm
tech.root: directcomp
ms.assetid: D47D6FA3-D5D2-47BD-8DE0-6E0EE08EE7C4
ms.date: 12/05/2018
ms.keywords: IDCompositionScaleTransform interface [DirectComposition],SetScaleY method, IDCompositionScaleTransform.SetScaleY, IDCompositionScaleTransform::SetScaleY, IDCompositionScaleTransform::SetScaleY(float), SetScaleY, SetScaleY method [DirectComposition], SetScaleY method [DirectComposition],IDCompositionScaleTransform interface, dcomp/IDCompositionScaleTransform::SetScaleY, directcomp.idcompositionscaletransform_setscaley_float
f1_keywords:
- dcomp/IDCompositionScaleTransform.SetScaleY
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
- IDCompositionScaleTransform.SetScaleY
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionScaleTransform::SetScaleY


## -description


Changes the value of the ScaleY property of a 2D scale transform. The ScaleY property specifies the scale factor along the y-axis.


## -parameters




### -param scaleY [in]

Type: <b>float</b>

The new y-axis scale factor.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>scaleY</i> parameter is NaN, positive infinity, or negative infinity.



If the ScaleY property was previously animated, this method removes the animation and sets the ScaleY property to the specified static value.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform">IDCompositionScaleTransform</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449048(v=vs.85)">IDCompositionScaleTransform::SetScaleX</a>
 

 

