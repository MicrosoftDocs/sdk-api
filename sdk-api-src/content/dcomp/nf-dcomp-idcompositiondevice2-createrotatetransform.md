---
UID: NF:dcomp.IDCompositionDevice2.CreateRotateTransform
title: IDCompositionDevice2::CreateRotateTransform (dcomp.h)
description: Creates a 2D rotation transform object. (IDCompositionDevice2.CreateRotateTransform)
helpviewer_keywords: ["CreateRotateTransform","CreateRotateTransform method [DirectComposition]","CreateRotateTransform method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","CreateRotateTransform method","IDCompositionDevice2.CreateRotateTransform","IDCompositionDevice2::CreateRotateTransform","dcomp/IDCompositionDevice2::CreateRotateTransform","directcomp.idcompositiondevice2_createrotatetransform"]
old-location: directcomp\idcompositiondevice2_createrotatetransform.htm
tech.root: directcomp
ms.assetid: C4F0187C-FB3C-447A-AD1E-5094004273F5
ms.date: 12/05/2018
ms.keywords: CreateRotateTransform, CreateRotateTransform method [DirectComposition], CreateRotateTransform method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateRotateTransform method, IDCompositionDevice2.CreateRotateTransform, IDCompositionDevice2::CreateRotateTransform, dcomp/IDCompositionDevice2::CreateRotateTransform, directcomp.idcompositiondevice2_createrotatetransform
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
 - IDCompositionDevice2::CreateRotateTransform
 - dcomp/IDCompositionDevice2::CreateRotateTransform
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
 - IDCompositionDevice2.CreateRotateTransform
---

# IDCompositionDevice2::CreateRotateTransform


## -description

Creates a 2D rotation transform object.

## -parameters

### -param rotateTransform [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform">IDCompositionRotateTransform</a>**</b>

The new rotation transform object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A new 2D rotation transform object has a static value of zero for the Angle, CenterX, and CenterY properties.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
