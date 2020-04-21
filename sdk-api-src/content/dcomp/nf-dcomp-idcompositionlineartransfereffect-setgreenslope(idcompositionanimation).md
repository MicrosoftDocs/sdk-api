---
UID: NF:dcomp.IDCompositionLinearTransferEffect.SetGreenSlope(IDCompositionAnimation)
title: IDCompositionLinearTransferEffect::SetGreenSlope(IDCompositionAnimation) (dcomp.h)
description: Sets the slope of the linear function for the green channel.helpviewer_keywords: ["IDCompositionLinearTransferEffect interface [DirectComposition]","SetGreenSlope method","IDCompositionLinearTransferEffect.SetGreenSlope","IDCompositionLinearTransferEffect.SetGreenSlope(IDCompositionAnimation)","IDCompositionLinearTransferEffect::SetGreenSlope","IDCompositionLinearTransferEffect::SetGreenSlope(IDCompositionAnimation)","SetGreenSlope","SetGreenSlope method [DirectComposition]","SetGreenSlope method [DirectComposition]","IDCompositionLinearTransferEffect interface","dcomp/IDCompositionLinearTransferEffect::SetGreenSlope","directcomp.idcompositionlineartransfereffect_setgreenslope_2"]
old-location: directcomp\idcompositionlineartransfereffect_setgreenslope_2.htm
tech.root: directcomp
ms.assetid: BAB60C7E-D2FA-4148-A1F6-5937D3AE746B
ms.date: 12/05/2018
ms.keywords: IDCompositionLinearTransferEffect interface [DirectComposition],SetGreenSlope method, IDCompositionLinearTransferEffect.SetGreenSlope, IDCompositionLinearTransferEffect.SetGreenSlope(IDCompositionAnimation), IDCompositionLinearTransferEffect::SetGreenSlope, IDCompositionLinearTransferEffect::SetGreenSlope(IDCompositionAnimation), SetGreenSlope, SetGreenSlope method [DirectComposition], SetGreenSlope method [DirectComposition],IDCompositionLinearTransferEffect interface, dcomp/IDCompositionLinearTransferEffect::SetGreenSlope, directcomp.idcompositionlineartransfereffect_setgreenslope_2
f1_keywords:
- dcomp/IDCompositionLinearTransferEffect.SetGreenSlope
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dcomp.dll
api_name:
- IDCompositionLinearTransferEffect.SetGreenSlope
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionLinearTransferEffect::SetGreenSlope(IDCompositionAnimation)


## -description


Sets the slope of the linear function for the green channel.


## -parameters




### -param animation [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the slope of the linear function for the green channel changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionlineartransfereffect">IDCompositionLinearTransferEffect</a>
 

 

