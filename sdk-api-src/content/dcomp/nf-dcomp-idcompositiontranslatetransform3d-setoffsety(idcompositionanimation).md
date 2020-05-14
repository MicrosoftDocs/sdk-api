---
UID: NF:dcomp.IDCompositionTranslateTransform3D.SetOffsetY(IDCompositionAnimation)
title: IDCompositionTranslateTransform3D::SetOffsetY(IDCompositionAnimation) (dcomp.h)
description: Animates the value of the OffsetY property of a 3D translation transform effect. The OffsetY property specifies the distance to translate along the y-axis.
helpviewer_keywords: ["IDCompositionTranslateTransform3D interface [DirectComposition]","SetOffsetY method","IDCompositionTranslateTransform3D.SetOffsetY","IDCompositionTranslateTransform3D.SetOffsetY(IDCompositionAnimation)","IDCompositionTranslateTransform3D::SetOffsetY","IDCompositionTranslateTransform3D::SetOffsetY(IDCompositionAnimation)","IDCompositionTranslateTransform3D::SetOffsetY(IDCompositionAnimation*)","SetOffsetY","SetOffsetY method [DirectComposition]","SetOffsetY method [DirectComposition]","IDCompositionTranslateTransform3D interface","dcomp/IDCompositionTranslateTransform3D::SetOffsetY","directcomp.idcompositiontranslatetransform3d_setoffsety_idcompositionanimation"]
old-location: directcomp\idcompositiontranslatetransform3d_setoffsety_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: D08FF13B-612A-4A60-B6C8-4EC1246F94E9
ms.date: 12/05/2018
ms.keywords: IDCompositionTranslateTransform3D interface [DirectComposition],SetOffsetY method, IDCompositionTranslateTransform3D.SetOffsetY, IDCompositionTranslateTransform3D.SetOffsetY(IDCompositionAnimation), IDCompositionTranslateTransform3D::SetOffsetY, IDCompositionTranslateTransform3D::SetOffsetY(IDCompositionAnimation), IDCompositionTranslateTransform3D::SetOffsetY(IDCompositionAnimation*), SetOffsetY, SetOffsetY method [DirectComposition], SetOffsetY method [DirectComposition],IDCompositionTranslateTransform3D interface, dcomp/IDCompositionTranslateTransform3D::SetOffsetY, directcomp.idcompositiontranslatetransform3d_setoffsety_idcompositionanimation
f1_keywords:
- dcomp/IDCompositionTranslateTransform3D.SetOffsetY
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

# IDCompositionTranslateTransform3D::SetOffsetY(IDCompositionAnimation)


## -description


Animates the value of the OffsetY property of a 3D translation transform effect. The OffsetY property specifies the distance to translate along the y-axis.


## -parameters




### -param animation [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the OffsetY property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the OffsetY property unless this method is called again. If the OffsetY property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d">IDCompositionTranslateTransform3D</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositiontranslatetransform3d-setoffsetx(float)">IDCompositionTranslateTransform3D::SetOffsetX</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositiontranslatetransform3d-setoffsetz(float)">IDCompositionTranslateTransform3D::SetOffsetZ</a>
 

 

