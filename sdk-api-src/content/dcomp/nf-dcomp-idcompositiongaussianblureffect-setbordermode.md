---
UID: NF:dcomp.IDCompositionGaussianBlurEffect.SetBorderMode
title: IDCompositionGaussianBlurEffect::SetBorderMode (dcomp.h)
description: Sets the mode used to calculate the border of the image.
helpviewer_keywords: ["IDCompositionGaussianBlurEffect interface [DirectComposition]","SetBorderMode method","IDCompositionGaussianBlurEffect.SetBorderMode","IDCompositionGaussianBlurEffect::SetBorderMode","SetBorderMode","SetBorderMode method [DirectComposition]","SetBorderMode method [DirectComposition]","IDCompositionGaussianBlurEffect interface","dcomp/IDCompositionGaussianBlurEffect::SetBorderMode","directcomp.idcompositiongaussianblureffect_setbordermode"]
old-location: directcomp\idcompositiongaussianblureffect_setbordermode.htm
tech.root: directcomp
ms.assetid: 34A96D63-E6F3-48F3-8105-A7E30C1D4E7D
ms.date: 12/05/2018
ms.keywords: IDCompositionGaussianBlurEffect interface [DirectComposition],SetBorderMode method, IDCompositionGaussianBlurEffect.SetBorderMode, IDCompositionGaussianBlurEffect::SetBorderMode, SetBorderMode, SetBorderMode method [DirectComposition], SetBorderMode method [DirectComposition],IDCompositionGaussianBlurEffect interface, dcomp/IDCompositionGaussianBlurEffect::SetBorderMode, directcomp.idcompositiongaussianblureffect_setbordermode
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
 - IDCompositionGaussianBlurEffect::SetBorderMode
 - dcomp/IDCompositionGaussianBlurEffect::SetBorderMode
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
 - IDCompositionGaussianBlurEffect.SetBorderMode
---

# IDCompositionGaussianBlurEffect::SetBorderMode


## -description

Sets the mode used to calculate the border of the image.

## -parameters

### -param mode [in]

Type: <b><a href="/windows/desktop/Direct2D/gaussian-blur">D2D1_BORDER_MODE</a></b>

The mode used to calculate the border of the image.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiongaussianblureffect">IDCompositionGaussianBlurEffect</a>