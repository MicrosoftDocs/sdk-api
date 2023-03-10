---
UID: NF:dcomp.IDCompositionDevice.CreateScaleTransform
title: IDCompositionDevice::CreateScaleTransform (dcomp.h)
description: The IDCompositionDevice::CreateScaleTransform method creates a 2D scale transform object.
helpviewer_keywords: ["CreateScaleTransform","CreateScaleTransform method [DirectComposition]","CreateScaleTransform method [DirectComposition]","IDCompositionDevice interface","IDCompositionDevice interface [DirectComposition]","CreateScaleTransform method","IDCompositionDevice.CreateScaleTransform","IDCompositionDevice::CreateScaleTransform","dcomp/IDCompositionDevice::CreateScaleTransform","directcomp.idcompositiondevice_createscaletransform"]
old-location: directcomp\idcompositiondevice_createscaletransform.htm
tech.root: directcomp
ms.assetid: b11673dd-87c1-43c9-8501-affa1fa64c08
ms.date: 06/23/2022
ms.keywords: CreateScaleTransform, CreateScaleTransform method [DirectComposition], CreateScaleTransform method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateScaleTransform method, IDCompositionDevice.CreateScaleTransform, IDCompositionDevice::CreateScaleTransform, dcomp/IDCompositionDevice::CreateScaleTransform, directcomp.idcompositiondevice_createscaletransform
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
 - IDCompositionDevice::CreateScaleTransform
 - dcomp/IDCompositionDevice::CreateScaleTransform
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
 - IDCompositionDevice.CreateScaleTransform
---

# IDCompositionDevice::CreateScaleTransform


## -description

Creates a 2D scale transform object.

## -parameters

### -param scaleTransform [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform">IDCompositionScaleTransform</a>**</b>

The new 2D scale transform object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A new 2D scale transform object has a static value of zero for the ScaleX, ScaleY, CenterX, and CenterY properties.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>