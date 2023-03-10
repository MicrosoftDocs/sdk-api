---
UID: NF:dcomp.IDCompositionLinearTransferEffect.SetBlueYIntercept(IDCompositionAnimation)
title: IDCompositionLinearTransferEffect::SetBlueYIntercept(IDCompositionAnimation) (dcomp.h)
description: The IDCompositionLinearTransferEffect::SetBlueYIntercept(IDCompositionAnimation) method sets the Y-intercept of the linear function for the blue channel.
helpviewer_keywords: ["IDCompositionLinearTransferEffect interface [DirectComposition]","SetBlueYIntercept method","IDCompositionLinearTransferEffect.SetBlueYIntercept","IDCompositionLinearTransferEffect.SetBlueYIntercept(IDCompositionAnimation)","IDCompositionLinearTransferEffect::SetBlueYIntercept","IDCompositionLinearTransferEffect::SetBlueYIntercept(IDCompositionAnimation)","SetBlueYIntercept","SetBlueYIntercept method [DirectComposition]","SetBlueYIntercept method [DirectComposition]","IDCompositionLinearTransferEffect interface","dcomp/IDCompositionLinearTransferEffect::SetBlueYIntercept","directcomp.idcompositionlineartransfereffect_setblueyintercept_2"]
old-location: directcomp\idcompositionlineartransfereffect_setblueyintercept_2.htm
tech.root: directcomp
ms.assetid: A75B26EB-CEA2-45E3-999D-9A49A261AA54
ms.date: 06/23/2022
ms.keywords: IDCompositionLinearTransferEffect interface [DirectComposition],SetBlueYIntercept method, IDCompositionLinearTransferEffect.SetBlueYIntercept, IDCompositionLinearTransferEffect.SetBlueYIntercept(IDCompositionAnimation), IDCompositionLinearTransferEffect::SetBlueYIntercept, IDCompositionLinearTransferEffect::SetBlueYIntercept(IDCompositionAnimation), SetBlueYIntercept, SetBlueYIntercept method [DirectComposition], SetBlueYIntercept method [DirectComposition],IDCompositionLinearTransferEffect interface, dcomp/IDCompositionLinearTransferEffect::SetBlueYIntercept, directcomp.idcompositionlineartransfereffect_setblueyintercept_2
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
 - IDCompositionLinearTransferEffect::SetBlueYIntercept
 - dcomp/IDCompositionLinearTransferEffect::SetBlueYIntercept
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
 - IDCompositionLinearTransferEffect.SetBlueYIntercept
---

# IDCompositionLinearTransferEffect::SetBlueYIntercept(IDCompositionAnimation)


## -description

Sets the Y-intercept of the linear function for the blue channel.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the Y-intercept of the linear function for the blue channel changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionlineartransfereffect">IDCompositionLinearTransferEffect</a>