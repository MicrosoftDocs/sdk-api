---
UID: NF:dcomp.IDCompositionArithmeticCompositeEffect.SetCoefficient1(IDCompositionAnimation)
title: IDCompositionArithmeticCompositeEffect::SetCoefficient1(IDCompositionAnimation) (dcomp.h)
author: windows-sdk-content
description: Sets the first coefficient for the equation used to composite the two input images.
old-location: directcomp\idcompositionarithmeticcompositeeffect_setcoefficient1_2.htm
tech.root: directcomp
ms.assetid: 475F112E-5A00-47C1-97F9-E2BB2CBD10D2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionArithmeticCompositeEffect interface [DirectComposition],SetCoefficient1 method, IDCompositionArithmeticCompositeEffect.SetCoefficient1, IDCompositionArithmeticCompositeEffect.SetCoefficient1(IDCompositionAnimation), IDCompositionArithmeticCompositeEffect::SetCoefficient1, IDCompositionArithmeticCompositeEffect::SetCoefficient1(IDCompositionAnimation), SetCoefficient1, SetCoefficient1 method [DirectComposition], SetCoefficient1 method [DirectComposition],IDCompositionArithmeticCompositeEffect interface, dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficient1, directcomp.idcompositionarithmeticcompositeeffect_setcoefficient1_2
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionArithmeticCompositeEffect.SetCoefficient1"
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
 - IDCompositionArithmeticCompositeEffect.SetCoefficient1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionArithmeticCompositeEffect::SetCoefficient1(IDCompositionAnimation)


## -description


Sets the first coefficient for the equation used to composite the two input images.


## -parameters




### -param animation [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the value changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionarithmeticcompositeeffect">IDCompositionArithmeticCompositeEffect</a>
 

 

