---
UID: NF:dcomp.IDCompositionDevice2.CreateTranslateTransform3D
title: IDCompositionDevice2::CreateTranslateTransform3D (dcomp.h)
description: Creates a 3D translation transform object.
helpviewer_keywords: ["CreateTranslateTransform3D","CreateTranslateTransform3D method [DirectComposition]","CreateTranslateTransform3D method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","CreateTranslateTransform3D method","IDCompositionDevice2.CreateTranslateTransform3D","IDCompositionDevice2::CreateTranslateTransform3D","dcomp/IDCompositionDevice2::CreateTranslateTransform3D","directcomp.idcompositiondevice2_createtranslatetransform3d"]
old-location: directcomp\idcompositiondevice2_createtranslatetransform3d.htm
tech.root: directcomp
ms.assetid: 7913D11B-5563-4921-B455-C34069AC7BCD
ms.date: 12/05/2018
ms.keywords: CreateTranslateTransform3D, CreateTranslateTransform3D method [DirectComposition], CreateTranslateTransform3D method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateTranslateTransform3D method, IDCompositionDevice2.CreateTranslateTransform3D, IDCompositionDevice2::CreateTranslateTransform3D, dcomp/IDCompositionDevice2::CreateTranslateTransform3D, directcomp.idcompositiondevice2_createtranslatetransform3d
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
 - IDCompositionDevice2::CreateTranslateTransform3D
 - dcomp/IDCompositionDevice2::CreateTranslateTransform3D
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
 - IDCompositionDevice2.CreateTranslateTransform3D
---

# IDCompositionDevice2::CreateTranslateTransform3D


## -description

Creates a 3D translation transform object.

## -parameters

### -param translateTransform3D [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d">IDCompositionTranslateTransform3D</a>**</b>

The new 3D translation transform object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A newly created 3D translation transform has a static value of 0 for the OffsetX, OffsetY, and OffsetZ properties.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d">IDCompositionEffectGroup::SetTransform3D</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>