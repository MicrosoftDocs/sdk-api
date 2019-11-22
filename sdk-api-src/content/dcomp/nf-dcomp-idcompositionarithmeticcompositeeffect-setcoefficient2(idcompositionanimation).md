---
UID: NF:dcomp.IDCompositionArithmeticCompositeEffect.SetCoefficient2(IDCompositionAnimation)
title: IDCompositionArithmeticCompositeEffect::SetCoefficient2(IDCompositionAnimation) (dcomp.h)

description: Sets the second coefficient for the equation used to composite the two input images.
old-location: directcomp\idcompositionarithmeticcompositeeffect_setcoefficient2_2.htm
tech.root: directcomp
ms.assetid: C1A43316-58FA-4F42-827D-AF11104F5E60

ms.date: 12/05/2018
ms.keywords: IDCompositionArithmeticCompositeEffect interface [DirectComposition],SetCoefficient2 method, IDCompositionArithmeticCompositeEffect.SetCoefficient2, IDCompositionArithmeticCompositeEffect.SetCoefficient2(IDCompositionAnimation), IDCompositionArithmeticCompositeEffect::SetCoefficient2, IDCompositionArithmeticCompositeEffect::SetCoefficient2(IDCompositionAnimation), SetCoefficient2, SetCoefficient2 method [DirectComposition], SetCoefficient2 method [DirectComposition],IDCompositionArithmeticCompositeEffect interface, dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficient2, directcomp.idcompositionarithmeticcompositeeffect_setcoefficient2_2
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionArithmeticCompositeEffect.SetCoefficient2"
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
 - IDCompositionArithmeticCompositeEffect.SetCoefficient2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionArithmeticCompositeEffect::SetCoefficient2(IDCompositionAnimation)


## -description


Sets the second coefficient for the equation used to composite the two input images.


## -parameters




### -param animation [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the value of the second coefficient changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionarithmeticcompositeeffect">IDCompositionArithmeticCompositeEffect</a>
 

 

