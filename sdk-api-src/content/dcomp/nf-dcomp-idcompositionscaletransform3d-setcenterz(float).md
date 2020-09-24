---
UID: NF:dcomp.IDCompositionScaleTransform3D.SetCenterZ(float)
title: IDCompositionScaleTransform3D::SetCenterZ (dcomp.h)
description: Changes the value of the CenterZ property of a 3D scale transform.
helpviewer_keywords: ["IDCompositionScaleTransform3D interface [DirectComposition]","SetCenterZ method","IDCompositionScaleTransform3D.SetCenterZ","IDCompositionScaleTransform3D::SetCenterZ","IDCompositionScaleTransform3D::SetCenterZ(float)","SetCenterZ","SetCenterZ method [DirectComposition]","SetCenterZ method [DirectComposition]","IDCompositionScaleTransform3D interface","dcomp/IDCompositionScaleTransform3D::SetCenterZ","directcomp.idcompositionscaletransform3d_setcenterz_float"]
old-location: directcomp\idcompositionscaletransform3d_setcenterz_float.htm
tech.root: directcomp
ms.assetid: 69610037-28CD-49DA-8633-C26986AD17E7
ms.date: 12/05/2018
ms.keywords: IDCompositionScaleTransform3D interface [DirectComposition],SetCenterZ method, IDCompositionScaleTransform3D.SetCenterZ, IDCompositionScaleTransform3D::SetCenterZ, IDCompositionScaleTransform3D::SetCenterZ(float), SetCenterZ, SetCenterZ method [DirectComposition], SetCenterZ method [DirectComposition],IDCompositionScaleTransform3D interface, dcomp/IDCompositionScaleTransform3D::SetCenterZ, directcomp.idcompositionscaletransform3d_setcenterz_float
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
 - IDCompositionScaleTransform3D::SetCenterZ
 - dcomp/IDCompositionScaleTransform3D::SetCenterZ
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
 - IDCompositionScaleTransform3D.SetCenterZ
---

# IDCompositionScaleTransform3D::SetCenterZ


## -description

Changes the value of the CenterZ property of a 3D scale transform.   The CenterZ property specifies the z-coordinate of the point about which scaling is performed.

## -parameters

### -param centerZ [in]

Type: <b>float</b>

The new z-coordinate of the center point.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>centerZ</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterZ property was previously animated, this method removes the animation and sets the CenterZ property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform">IDCompositionScaleTransform3D</a>



<a href="/previous-versions/windows/desktop/legacy/hh448998(v=vs.85)">IDCompositionScaleTransform3D::SetCenterX</a>



<a href="/previous-versions/windows/desktop/legacy/hh449006(v=vs.85)">IDCompositionScaleTransform3D::SetCenterY</a>