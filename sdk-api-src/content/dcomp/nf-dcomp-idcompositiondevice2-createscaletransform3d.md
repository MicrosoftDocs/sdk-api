---
UID: NF:dcomp.IDCompositionDevice2.CreateScaleTransform3D
title: IDCompositionDevice2::CreateScaleTransform3D (dcomp.h)
description: Creates a 3D scale transform object.
helpviewer_keywords: ["CreateScaleTransform3D","CreateScaleTransform3D method [DirectComposition]","CreateScaleTransform3D method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","CreateScaleTransform3D method","IDCompositionDevice2.CreateScaleTransform3D","IDCompositionDevice2::CreateScaleTransform3D","dcomp/IDCompositionDevice2::CreateScaleTransform3D","directcomp.idcompositiondevice2_createscaletransform3d"]
old-location: directcomp\idcompositiondevice2_createscaletransform3d.htm
tech.root: directcomp
ms.assetid: 33B2C0D6-52D6-4443-9F30-A86C0F7BA627
ms.date: 12/05/2018
ms.keywords: CreateScaleTransform3D, CreateScaleTransform3D method [DirectComposition], CreateScaleTransform3D method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateScaleTransform3D method, IDCompositionDevice2.CreateScaleTransform3D, IDCompositionDevice2::CreateScaleTransform3D, dcomp/IDCompositionDevice2::CreateScaleTransform3D, directcomp.idcompositiondevice2_createscaletransform3d
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDCompositionDevice2::CreateScaleTransform3D
 - dcomp/IDCompositionDevice2::CreateScaleTransform3D
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
 - IDCompositionDevice2.CreateScaleTransform3D
---

# IDCompositionDevice2::CreateScaleTransform3D


## -description

Creates a 3D scale transform object.

## -parameters

### -param scaleTransform3D [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform3d">IDCompositionScaleTransform3D</a>**</b>

The new 3D scale transform object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A new 3D scale transform object has a static value of 1.0 for the ScaleX, ScaleY, and ScaleZ properties.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d">IDCompositionEffectGroup::SetTransform3D</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>