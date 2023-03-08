---
UID: NF:dcomp.IDCompositionLinearTransferEffect.SetRedYIntercept(IDCompositionAnimation)
title: IDCompositionLinearTransferEffect::SetRedYIntercept(IDCompositionAnimation) (dcomp.h)
description: Sets the Y-intercept of the linear function for the red channel. (overload 2/2)
helpviewer_keywords: ["IDCompositionLinearTransferEffect interface [DirectComposition]","SetRedYIntercept method","IDCompositionLinearTransferEffect.SetRedYIntercept","IDCompositionLinearTransferEffect.SetRedYIntercept(IDCompositionAnimation)","IDCompositionLinearTransferEffect::SetRedYIntercept","IDCompositionLinearTransferEffect::SetRedYIntercept(IDCompositionAnimation)","SetRedYIntercept","SetRedYIntercept method [DirectComposition]","SetRedYIntercept method [DirectComposition]","IDCompositionLinearTransferEffect interface","dcomp/IDCompositionLinearTransferEffect::SetRedYIntercept","directcomp.idcompositionlineartransfereffect_setredyintercept_2"]
old-location: directcomp\idcompositionlineartransfereffect_setredyintercept_2.htm
tech.root: directcomp
ms.assetid: 29D4DF13-834C-4BBE-818A-64770C68CB69
ms.date: 12/05/2018
ms.keywords: IDCompositionLinearTransferEffect interface [DirectComposition],SetRedYIntercept method, IDCompositionLinearTransferEffect.SetRedYIntercept, IDCompositionLinearTransferEffect.SetRedYIntercept(IDCompositionAnimation), IDCompositionLinearTransferEffect::SetRedYIntercept, IDCompositionLinearTransferEffect::SetRedYIntercept(IDCompositionAnimation), SetRedYIntercept, SetRedYIntercept method [DirectComposition], SetRedYIntercept method [DirectComposition],IDCompositionLinearTransferEffect interface, dcomp/IDCompositionLinearTransferEffect::SetRedYIntercept, directcomp.idcompositionlineartransfereffect_setredyintercept_2
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
 - IDCompositionLinearTransferEffect::SetRedYIntercept
 - dcomp/IDCompositionLinearTransferEffect::SetRedYIntercept
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
 - IDCompositionLinearTransferEffect.SetRedYIntercept
---

# IDCompositionLinearTransferEffect::SetRedYIntercept(IDCompositionAnimation)


## -description

Sets the Y-intercept of the linear function for the red channel.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the Y-intercept of the linear function for the red channel changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionlineartransfereffect">IDCompositionLinearTransferEffect</a>
