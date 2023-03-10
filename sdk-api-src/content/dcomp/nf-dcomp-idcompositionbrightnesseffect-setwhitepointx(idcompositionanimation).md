---
UID: NF:dcomp.IDCompositionBrightnessEffect.SetWhitePointX(IDCompositionAnimation)
title: IDCompositionBrightnessEffect::SetWhitePointX(IDCompositionAnimation) (dcomp.h)
description: Sets the x value of the white point. (overload 1/2)
helpviewer_keywords: ["IDCompositionBrightnessEffect interface [DirectComposition]","SetWhitePointX method","IDCompositionBrightnessEffect.SetWhitePointX","IDCompositionBrightnessEffect.SetWhitePointX(IDCompositionAnimation)","IDCompositionBrightnessEffect::SetWhitePointX","IDCompositionBrightnessEffect::SetWhitePointX(IDCompositionAnimation)","SetWhitePointX","SetWhitePointX method [DirectComposition]","SetWhitePointX method [DirectComposition]","IDCompositionBrightnessEffect interface","dcomp/IDCompositionBrightnessEffect::SetWhitePointX","directcomp.idcompositionbrightnesseffect_setwhitepointx_2"]
old-location: directcomp\idcompositionbrightnesseffect_setwhitepointx_2.htm
tech.root: directcomp
ms.assetid: 8724AB82-ED50-47C7-A4AE-31A12E3834F5
ms.date: 12/05/2018
ms.keywords: IDCompositionBrightnessEffect interface [DirectComposition],SetWhitePointX method, IDCompositionBrightnessEffect.SetWhitePointX, IDCompositionBrightnessEffect.SetWhitePointX(IDCompositionAnimation), IDCompositionBrightnessEffect::SetWhitePointX, IDCompositionBrightnessEffect::SetWhitePointX(IDCompositionAnimation), SetWhitePointX, SetWhitePointX method [DirectComposition], SetWhitePointX method [DirectComposition],IDCompositionBrightnessEffect interface, dcomp/IDCompositionBrightnessEffect::SetWhitePointX, directcomp.idcompositionbrightnesseffect_setwhitepointx_2
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
 - IDCompositionBrightnessEffect::SetWhitePointX
 - dcomp/IDCompositionBrightnessEffect::SetWhitePointX
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
 - IDCompositionBrightnessEffect.SetWhitePointX
---

# IDCompositionBrightnessEffect::SetWhitePointX(IDCompositionAnimation)


## -description

Sets the x value of the white point.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the x value of the white point changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionbrightnesseffect">IDCompositionBrightnessEffect</a>
