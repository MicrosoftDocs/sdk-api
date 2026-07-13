---
UID: NF:dcomp.IDCompositionBrightnessEffect.SetWhitePointY(IDCompositionAnimation)
title: IDCompositionBrightnessEffect::SetWhitePointY(IDCompositionAnimation) (dcomp.h)
description: Sets the y value of the white point. (overload 1/2)
helpviewer_keywords: ["IDCompositionBrightnessEffect interface [DirectComposition]","SetWhitePointY method","IDCompositionBrightnessEffect.SetWhitePointY","IDCompositionBrightnessEffect.SetWhitePointY(IDCompositionAnimation)","IDCompositionBrightnessEffect::SetWhitePointY","IDCompositionBrightnessEffect::SetWhitePointY(IDCompositionAnimation)","SetWhitePointY","SetWhitePointY method [DirectComposition]","SetWhitePointY method [DirectComposition]","IDCompositionBrightnessEffect interface","dcomp/IDCompositionBrightnessEffect::SetWhitePointY","directcomp.idcompositionbrightnesseffect_setwhitepointy_2"]
old-location: directcomp\idcompositionbrightnesseffect_setwhitepointy_2.htm
tech.root: directcomp
ms.assetid: 4B946372-578B-4799-AC61-58EEAAC5C267
ms.date: 12/05/2018
ms.keywords: IDCompositionBrightnessEffect interface [DirectComposition],SetWhitePointY method, IDCompositionBrightnessEffect.SetWhitePointY, IDCompositionBrightnessEffect.SetWhitePointY(IDCompositionAnimation), IDCompositionBrightnessEffect::SetWhitePointY, IDCompositionBrightnessEffect::SetWhitePointY(IDCompositionAnimation), SetWhitePointY, SetWhitePointY method [DirectComposition], SetWhitePointY method [DirectComposition],IDCompositionBrightnessEffect interface, dcomp/IDCompositionBrightnessEffect::SetWhitePointY, directcomp.idcompositionbrightnesseffect_setwhitepointy_2
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
 - IDCompositionBrightnessEffect::SetWhitePointY
 - dcomp/IDCompositionBrightnessEffect::SetWhitePointY
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
 - IDCompositionBrightnessEffect.SetWhitePointY
---

# IDCompositionBrightnessEffect::SetWhitePointY(IDCompositionAnimation)


## -description

Sets the y value of the white point.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the y value of the white point changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionbrightnesseffect">IDCompositionBrightnessEffect</a>
