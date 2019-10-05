---
UID: NF:dcomp.IDCompositionArithmeticCompositeEffect.SetCoefficients
title: IDCompositionArithmeticCompositeEffect::SetCoefficients (dcomp.h)
author: windows-sdk-content
description: Sets the coefficients for the equation used to composite the two input images.
old-location: directcomp\idcompositionarithmeticcompositeeffect_setcoefficients.htm
tech.root: directcomp
ms.assetid: 02A98C38-1D6E-43ED-8744-D3029F4BF573
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionArithmeticCompositeEffect interface [DirectComposition],SetCoefficients method, IDCompositionArithmeticCompositeEffect.SetCoefficients, IDCompositionArithmeticCompositeEffect::SetCoefficients, SetCoefficients, SetCoefficients method [DirectComposition], SetCoefficients method [DirectComposition],IDCompositionArithmeticCompositeEffect interface, dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficients, directcomp.idcompositionarithmeticcompositeeffect_setcoefficients
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionArithmeticCompositeEffect.SetCoefficients"
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
 - IDCompositionArithmeticCompositeEffect.SetCoefficients
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionArithmeticCompositeEffect::SetCoefficients


## -description


Sets the coefficients for the equation used to composite the two input images.


## -parameters




### -param coefficients [in, ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f">D2D1_VECTOR_4F</a></b>

The coefficients for the equation used to composite the two input images.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionarithmeticcompositeeffect">IDCompositionArithmeticCompositeEffect</a>
 

 

