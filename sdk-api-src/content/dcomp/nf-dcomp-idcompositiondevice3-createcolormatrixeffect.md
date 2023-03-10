---
UID: NF:dcomp.IDCompositionDevice3.CreateColorMatrixEffect
title: IDCompositionDevice3::CreateColorMatrixEffect (dcomp.h)
description: Creates an instance of IDCompositionColorMatrixEffect.
helpviewer_keywords: ["CreateColorMatrixEffect","CreateColorMatrixEffect method [DirectComposition]","CreateColorMatrixEffect method [DirectComposition]","IDCompositionDevice3 interface","IDCompositionDevice3 interface [DirectComposition]","CreateColorMatrixEffect method","IDCompositionDevice3.CreateColorMatrixEffect","IDCompositionDevice3::CreateColorMatrixEffect","dcomp/IDCompositionDevice3::CreateColorMatrixEffect","directcomp.idcompositiondevice3_createcolormatrixeffect"]
old-location: directcomp\idcompositiondevice3_createcolormatrixeffect.htm
tech.root: directcomp
ms.assetid: A286F5C1-764F-4FAF-B2D2-92820BD2E709
ms.date: 12/05/2018
ms.keywords: CreateColorMatrixEffect, CreateColorMatrixEffect method [DirectComposition], CreateColorMatrixEffect method [DirectComposition],IDCompositionDevice3 interface, IDCompositionDevice3 interface [DirectComposition],CreateColorMatrixEffect method, IDCompositionDevice3.CreateColorMatrixEffect, IDCompositionDevice3::CreateColorMatrixEffect, dcomp/IDCompositionDevice3::CreateColorMatrixEffect, directcomp.idcompositiondevice3_createcolormatrixeffect
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDCompositionDevice3::CreateColorMatrixEffect
 - dcomp/IDCompositionDevice3::CreateColorMatrixEffect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dcomp.dll
api_name:
 - IDCompositionDevice3.CreateColorMatrixEffect
---

# IDCompositionDevice3::CreateColorMatrixEffect


## -description

Creates an instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioncolormatrixeffect">IDCompositionColorMatrixEffect</a>.

## -parameters

### -param colorMatrixEffect [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioncolormatrixeffect">IDCompositionColorMatrixEffect</a>**</b>

Receives the created instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioncolormatrixeffect">IDCompositionColorMatrixEffect</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice3">IDCompositionDevice3</a>