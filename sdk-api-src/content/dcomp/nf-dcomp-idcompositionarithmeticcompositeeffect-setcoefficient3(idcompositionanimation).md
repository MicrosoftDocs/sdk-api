---
UID: NF:dcomp.IDCompositionArithmeticCompositeEffect.SetCoefficient3(IDCompositionAnimation)
title: IDCompositionArithmeticCompositeEffect::SetCoefficient3(IDCompositionAnimation) (dcomp.h)
description: Sets the third coefficient for the equation used to composite the two input images. (overload 2/2)
helpviewer_keywords: ["IDCompositionArithmeticCompositeEffect interface [DirectComposition]","SetCoefficient3 method","IDCompositionArithmeticCompositeEffect.SetCoefficient3","IDCompositionArithmeticCompositeEffect.SetCoefficient3(IDCompositionAnimation)","IDCompositionArithmeticCompositeEffect::SetCoefficient3","IDCompositionArithmeticCompositeEffect::SetCoefficient3(IDCompositionAnimation)","SetCoefficient3","SetCoefficient3 method [DirectComposition]","SetCoefficient3 method [DirectComposition]","IDCompositionArithmeticCompositeEffect interface","dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficient3","directcomp.idcompositionarithmeticcompositeeffect_setcoefficient3_2"]
old-location: directcomp\idcompositionarithmeticcompositeeffect_setcoefficient3_2.htm
tech.root: directcomp
ms.assetid: C08978C7-7028-4E48-B19F-1FC682E0FB82
ms.date: 12/05/2018
ms.keywords: IDCompositionArithmeticCompositeEffect interface [DirectComposition],SetCoefficient3 method, IDCompositionArithmeticCompositeEffect.SetCoefficient3, IDCompositionArithmeticCompositeEffect.SetCoefficient3(IDCompositionAnimation), IDCompositionArithmeticCompositeEffect::SetCoefficient3, IDCompositionArithmeticCompositeEffect::SetCoefficient3(IDCompositionAnimation), SetCoefficient3, SetCoefficient3 method [DirectComposition], SetCoefficient3 method [DirectComposition],IDCompositionArithmeticCompositeEffect interface, dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficient3, directcomp.idcompositionarithmeticcompositeeffect_setcoefficient3_2
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
 - IDCompositionArithmeticCompositeEffect::SetCoefficient3
 - dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficient3
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
 - IDCompositionArithmeticCompositeEffect.SetCoefficient3
---

# IDCompositionArithmeticCompositeEffect::SetCoefficient3(IDCompositionAnimation)


## -description

Sets the third coefficient for the equation used to composite the two input images.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the value of the third coefficient changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionarithmeticcompositeeffect">IDCompositionArithmeticCompositeEffect</a>
