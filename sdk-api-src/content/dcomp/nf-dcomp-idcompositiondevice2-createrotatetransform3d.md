---
UID: NF:dcomp.IDCompositionDevice2.CreateRotateTransform3D
title: IDCompositionDevice2::CreateRotateTransform3D (dcomp.h)
description: Creates a 3D rotation transform object.
helpviewer_keywords: ["CreateRotateTransform3D","CreateRotateTransform3D method [DirectComposition]","CreateRotateTransform3D method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","CreateRotateTransform3D method","IDCompositionDevice2.CreateRotateTransform3D","IDCompositionDevice2::CreateRotateTransform3D","dcomp/IDCompositionDevice2::CreateRotateTransform3D","directcomp.idcompositiondevice2_createrotatetransform3d"]
old-location: directcomp\idcompositiondevice2_createrotatetransform3d.htm
tech.root: directcomp
ms.assetid: F665A6EB-2EF2-4B65-BD89-84F78B5AD468
ms.date: 12/05/2018
ms.keywords: CreateRotateTransform3D, CreateRotateTransform3D method [DirectComposition], CreateRotateTransform3D method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateRotateTransform3D method, IDCompositionDevice2.CreateRotateTransform3D, IDCompositionDevice2::CreateRotateTransform3D, dcomp/IDCompositionDevice2::CreateRotateTransform3D, directcomp.idcompositiondevice2_createrotatetransform3d
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
 - IDCompositionDevice2::CreateRotateTransform3D
 - dcomp/IDCompositionDevice2::CreateRotateTransform3D
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
 - IDCompositionDevice2.CreateRotateTransform3D
---

# IDCompositionDevice2::CreateRotateTransform3D


## -description

Creates a 3D rotation transform object.

## -parameters

### -param rotateTransform3D [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>**</b>

The new 3D rotation transform object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A new 3D rotation transform object has a default static value of zero for the Angle, CenterX, CenterY, CenterZ, AxisX, and AxisY properties, and a default static value of 1.0 for the AxisZ property.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionEffectGroup::SetTransform</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>