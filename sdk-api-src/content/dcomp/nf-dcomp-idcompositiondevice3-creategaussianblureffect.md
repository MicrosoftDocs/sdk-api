---
UID: NF:dcomp.IDCompositionDevice3.CreateGaussianBlurEffect
title: IDCompositionDevice3::CreateGaussianBlurEffect (dcomp.h)
description: Creates an instance of IDCompositionGaussianBlurEffect.
helpviewer_keywords: ["CreateGaussianBlurEffect","CreateGaussianBlurEffect method [DirectComposition]","CreateGaussianBlurEffect method [DirectComposition]","IDCompositionDevice3 interface","IDCompositionDevice3 interface [DirectComposition]","CreateGaussianBlurEffect method","IDCompositionDevice3.CreateGaussianBlurEffect","IDCompositionDevice3::CreateGaussianBlurEffect","dcomp/IDCompositionDevice3::CreateGaussianBlurEffect","directcomp.idcompositiondevice3_creategaussianblureffect"]
old-location: directcomp\idcompositiondevice3_creategaussianblureffect.htm
tech.root: directcomp
ms.assetid: D05C7A70-107A-4246-9391-7B00ECAA0B80
ms.date: 12/05/2018
ms.keywords: CreateGaussianBlurEffect, CreateGaussianBlurEffect method [DirectComposition], CreateGaussianBlurEffect method [DirectComposition],IDCompositionDevice3 interface, IDCompositionDevice3 interface [DirectComposition],CreateGaussianBlurEffect method, IDCompositionDevice3.CreateGaussianBlurEffect, IDCompositionDevice3::CreateGaussianBlurEffect, dcomp/IDCompositionDevice3::CreateGaussianBlurEffect, directcomp.idcompositiondevice3_creategaussianblureffect
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
 - IDCompositionDevice3::CreateGaussianBlurEffect
 - dcomp/IDCompositionDevice3::CreateGaussianBlurEffect
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
 - IDCompositionDevice3.CreateGaussianBlurEffect
---

# IDCompositionDevice3::CreateGaussianBlurEffect


## -description

Creates an instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiongaussianblureffect">IDCompositionGaussianBlurEffect</a>.

## -parameters

### -param gaussianBlurEffect [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiongaussianblureffect">IDCompositionGaussianBlurEffect</a>**</b>

Receives the created instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiongaussianblureffect">IDCompositionGaussianBlurEffect</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice3">IDCompositionDevice3</a>