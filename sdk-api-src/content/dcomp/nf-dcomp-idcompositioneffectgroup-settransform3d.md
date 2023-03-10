---
UID: NF:dcomp.IDCompositionEffectGroup.SetTransform3D
title: IDCompositionEffectGroup::SetTransform3D (dcomp.h)
description: Sets the 3D transformation effect object that modifies the rasterization of the visuals that this effect group is applied to.
helpviewer_keywords: ["IDCompositionEffectGroup interface [DirectComposition]","SetTransform3D method","IDCompositionEffectGroup.SetTransform3D","IDCompositionEffectGroup::SetTransform3D","SetTransform3D","SetTransform3D method [DirectComposition]","SetTransform3D method [DirectComposition]","IDCompositionEffectGroup interface","dcomp/IDCompositionEffectGroup::SetTransform3D","directcomp.idcompositioneffectgroup_settransform3d"]
old-location: directcomp\idcompositioneffectgroup_settransform3d.htm
tech.root: directcomp
ms.assetid: 40935581-D45C-496B-90B9-152963F0B55A
ms.date: 12/05/2018
ms.keywords: IDCompositionEffectGroup interface [DirectComposition],SetTransform3D method, IDCompositionEffectGroup.SetTransform3D, IDCompositionEffectGroup::SetTransform3D, SetTransform3D, SetTransform3D method [DirectComposition], SetTransform3D method [DirectComposition],IDCompositionEffectGroup interface, dcomp/IDCompositionEffectGroup::SetTransform3D, directcomp.idcompositioneffectgroup_settransform3d
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionEffectGroup::SetTransform3D
 - dcomp/IDCompositionEffectGroup::SetTransform3D
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionEffectGroup.SetTransform3D
---

# IDCompositionEffectGroup::SetTransform3D


## -description

Sets the 3D transformation effect object that modifies the rasterization of the visuals that this effect group is applied to.

## -parameters

### -param transform3D [in, optional]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>*</b>

Pointer to an <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a> interface or one of its derived interfaces. This parameter can be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if <i>transform3D</i> is an invalid pointer, or if the pointer was not created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as this effect group. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.



If the <i>transform3D</i> parameter is NULL, the effect group does not apply any perspective transformations to the visuals. Setting the transform to NULL is equivalent to setting the transform to an <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionmatrixtransform3d">IDCompositionMatrixTransform3D</a> object where the specified matrix is the identity matrix. However, an application should use a NULL transform whenever possible because it is slightly faster.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffectgroup">IDCompositionEffectGroup</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionmatrixtransform3d">IDCompositionMatrixTransform3D</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform3d">IDCompositionScaleTransform3D</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d">IDCompositionTranslateTransform3D</a>