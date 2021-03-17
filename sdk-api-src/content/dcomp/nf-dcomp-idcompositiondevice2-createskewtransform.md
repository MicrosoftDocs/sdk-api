---
UID: NF:dcomp.IDCompositionDevice2.CreateSkewTransform
title: IDCompositionDevice2::CreateSkewTransform (dcomp.h)
description: Creates a 2D skew transform object.
helpviewer_keywords: ["CreateSkewTransform","CreateSkewTransform method [DirectComposition]","CreateSkewTransform method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","CreateSkewTransform method","IDCompositionDevice2.CreateSkewTransform","IDCompositionDevice2::CreateSkewTransform","dcomp/IDCompositionDevice2::CreateSkewTransform","directcomp.idcompositiondevice2_createskewtransform"]
old-location: directcomp\idcompositiondevice2_createskewtransform.htm
tech.root: directcomp
ms.assetid: 10700E97-C799-4FC0-8300-B5347CC67AC3
ms.date: 12/05/2018
ms.keywords: CreateSkewTransform, CreateSkewTransform method [DirectComposition], CreateSkewTransform method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateSkewTransform method, IDCompositionDevice2.CreateSkewTransform, IDCompositionDevice2::CreateSkewTransform, dcomp/IDCompositionDevice2::CreateSkewTransform, directcomp.idcompositiondevice2_createskewtransform
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
 - IDCompositionDevice2::CreateSkewTransform
 - dcomp/IDCompositionDevice2::CreateSkewTransform
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
 - IDCompositionDevice2.CreateSkewTransform
---

# IDCompositionDevice2::CreateSkewTransform


## -description

Creates a 2D skew transform object.

## -parameters

### -param skewTransform [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionskewtransform">IDCompositionSkewTransform</a>**</b>

The new 2D skew transform object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A new 2D skew transform object has a static value of zero for the AngleX, AngleY, CenterX, and CenterY properties.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>