---
UID: NF:dcomp.IDCompositionTranslateTransform3D.SetOffsetZ(float)
title: IDCompositionTranslateTransform3D::SetOffsetZ (dcomp.h)
description: Changes the value of the OffsetZ property of a 3D translation transform effect. The OffsetZ property specifies the distance to translate along the z-axis.
helpviewer_keywords: ["IDCompositionTranslateTransform3D interface [DirectComposition]","SetOffsetZ method","IDCompositionTranslateTransform3D.SetOffsetZ","IDCompositionTranslateTransform3D::SetOffsetZ","IDCompositionTranslateTransform3D::SetOffsetZ(float)","SetOffsetZ","SetOffsetZ method [DirectComposition]","SetOffsetZ method [DirectComposition]","IDCompositionTranslateTransform3D interface","dcomp/IDCompositionTranslateTransform3D::SetOffsetZ","directcomp.idcompositiontranslatetransform3d_setoffsetz_float"]
old-location: directcomp\idcompositiontranslatetransform3d_setoffsetz_float.htm
tech.root: directcomp
ms.assetid: 98FC07F4-BD13-448A-8421-9049CF9C0850
ms.date: 12/05/2018
ms.keywords: IDCompositionTranslateTransform3D interface [DirectComposition],SetOffsetZ method, IDCompositionTranslateTransform3D.SetOffsetZ, IDCompositionTranslateTransform3D::SetOffsetZ, IDCompositionTranslateTransform3D::SetOffsetZ(float), SetOffsetZ, SetOffsetZ method [DirectComposition], SetOffsetZ method [DirectComposition],IDCompositionTranslateTransform3D interface, dcomp/IDCompositionTranslateTransform3D::SetOffsetZ, directcomp.idcompositiontranslatetransform3d_setoffsetz_float
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
 - IDCompositionTranslateTransform3D::SetOffsetZ
 - dcomp/IDCompositionTranslateTransform3D::SetOffsetZ
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
 - IDCompositionTranslateTransform3D.SetOffsetZ
---

# IDCompositionTranslateTransform3D::SetOffsetZ


## -description

Changes the value of the OffsetZ property of a 3D translation transform effect. The OffsetZ property specifies the distance to translate along the z-axis.

## -parameters

### -param offsetZ [in]

Type: <b>float</b>

The distance to translate along the z-axis, in pixels.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>offsetZ</i> parameter is NaN, positive infinity, or negative infinity.



If the OffsetZ property was previously animated, this method removes the animation and sets the OffsetZ property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d">IDCompositionTranslateTransform3D</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositiontranslatetransform3d-setoffsetx(float)">IDCompositionTranslateTransform3D::SetOffsetX</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositiontranslatetransform3d-setoffsety(float)">IDCompositionTranslateTransform3D::SetOffsetY</a>