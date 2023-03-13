---
UID: NF:dcomp.IDCompositionLinearTransferEffect.SetAlphaSlope(IDCompositionAnimation)
title: IDCompositionLinearTransferEffect::SetAlphaSlope(IDCompositionAnimation) (dcomp.h)
description: The IDCompositionLinearTransferEffect::SetAlphaSlope(IDCompositionAnimation) method sets the slope of the linear function for the alpha channel.
helpviewer_keywords: ["IDCompositionLinearTransferEffect interface [DirectComposition]","SetAlphaSlope method","IDCompositionLinearTransferEffect.SetAlphaSlope","IDCompositionLinearTransferEffect.SetAlphaSlope(IDCompositionAnimation)","IDCompositionLinearTransferEffect::SetAlphaSlope","IDCompositionLinearTransferEffect::SetAlphaSlope(IDCompositionAnimation)","SetAlphaSlope","SetAlphaSlope method [DirectComposition]","SetAlphaSlope method [DirectComposition]","IDCompositionLinearTransferEffect interface","dcomp/IDCompositionLinearTransferEffect::SetAlphaSlope","directcomp.idcompositionlineartransfereffect_setalphaslope_2"]
old-location: directcomp\idcompositionlineartransfereffect_setalphaslope_2.htm
tech.root: directcomp
ms.assetid: 8992B338-5426-4DB7-8ACB-8E5E3C702BFF
ms.date: 06/23/2022
ms.keywords: IDCompositionLinearTransferEffect interface [DirectComposition],SetAlphaSlope method, IDCompositionLinearTransferEffect.SetAlphaSlope, IDCompositionLinearTransferEffect.SetAlphaSlope(IDCompositionAnimation), IDCompositionLinearTransferEffect::SetAlphaSlope, IDCompositionLinearTransferEffect::SetAlphaSlope(IDCompositionAnimation), SetAlphaSlope, SetAlphaSlope method [DirectComposition], SetAlphaSlope method [DirectComposition],IDCompositionLinearTransferEffect interface, dcomp/IDCompositionLinearTransferEffect::SetAlphaSlope, directcomp.idcompositionlineartransfereffect_setalphaslope_2
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
 - IDCompositionLinearTransferEffect::SetAlphaSlope
 - dcomp/IDCompositionLinearTransferEffect::SetAlphaSlope
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
 - IDCompositionLinearTransferEffect.SetAlphaSlope
---

# IDCompositionLinearTransferEffect::SetAlphaSlope(IDCompositionAnimation)


## -description

Sets the slope of the linear function for the alpha channel.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the slope of the linear function for the alpha channel changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionlineartransfereffect">IDCompositionLinearTransferEffect</a>