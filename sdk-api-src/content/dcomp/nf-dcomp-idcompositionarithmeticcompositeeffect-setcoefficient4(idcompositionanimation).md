---
UID: NF:dcomp.IDCompositionArithmeticCompositeEffect.SetCoefficient4(IDCompositionAnimation)
title: IDCompositionArithmeticCompositeEffect::SetCoefficient4(IDCompositionAnimation) (dcomp.h)
description: Sets the fourth coefficient for the equation used to composite the two input images. (overload 1/2)
helpviewer_keywords: ["IDCompositionArithmeticCompositeEffect interface [DirectComposition]","SetCoefficient4 method","IDCompositionArithmeticCompositeEffect.SetCoefficient4","IDCompositionArithmeticCompositeEffect.SetCoefficient4(IDCompositionAnimation)","IDCompositionArithmeticCompositeEffect::SetCoefficient4","IDCompositionArithmeticCompositeEffect::SetCoefficient4(IDCompositionAnimation)","SetCoefficient4","SetCoefficient4 method [DirectComposition]","SetCoefficient4 method [DirectComposition]","IDCompositionArithmeticCompositeEffect interface","dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficient4","directcomp.idcompositionarithmeticcompositeeffect_setcoefficient4_2"]
old-location: directcomp\idcompositionarithmeticcompositeeffect_setcoefficient4_2.htm
tech.root: directcomp
ms.assetid: F495A5CC-4FAA-482F-83E4-C6CF887EA00F
ms.date: 12/05/2018
ms.keywords: IDCompositionArithmeticCompositeEffect interface [DirectComposition],SetCoefficient4 method, IDCompositionArithmeticCompositeEffect.SetCoefficient4, IDCompositionArithmeticCompositeEffect.SetCoefficient4(IDCompositionAnimation), IDCompositionArithmeticCompositeEffect::SetCoefficient4, IDCompositionArithmeticCompositeEffect::SetCoefficient4(IDCompositionAnimation), SetCoefficient4, SetCoefficient4 method [DirectComposition], SetCoefficient4 method [DirectComposition],IDCompositionArithmeticCompositeEffect interface, dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficient4, directcomp.idcompositionarithmeticcompositeeffect_setcoefficient4_2
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
 - IDCompositionArithmeticCompositeEffect::SetCoefficient4
 - dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficient4
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
 - IDCompositionArithmeticCompositeEffect.SetCoefficient4
---

# IDCompositionArithmeticCompositeEffect::SetCoefficient4(IDCompositionAnimation)


## -description

Sets the fourth coefficient for the equation used to composite the two input images.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the value of the fourth coefficient changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionarithmeticcompositeeffect">IDCompositionArithmeticCompositeEffect</a>
