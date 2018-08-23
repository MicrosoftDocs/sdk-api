---
UID: NF:dcomp.IDCompositionArithmeticCompositeEffect.SetCoefficients
title: IDCompositionArithmeticCompositeEffect::SetCoefficients
author: windows-sdk-content
description: Sets the coefficients for the equation used to composite the two input images.
old-location: directcomp\idcompositionarithmeticcompositeeffect_setcoefficients.htm
old-project: directcomp
ms.assetid: 02A98C38-1D6E-43ED-8744-D3029F4BF573
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionArithmeticCompositeEffect interface [DirectComposition],SetCoefficients method, IDCompositionArithmeticCompositeEffect.SetCoefficients, IDCompositionArithmeticCompositeEffect::SetCoefficients, SetCoefficients, SetCoefficients method [DirectComposition], SetCoefficients method [DirectComposition],IDCompositionArithmeticCompositeEffect interface, dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficients, directcomp.idcompositionarithmeticcompositeeffect_setcoefficients
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D_VECTOR_4F
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionArithmeticCompositeEffect.SetCoefficients
product: Windows
targetos: Windows
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# IDCompositionArithmeticCompositeEffect::SetCoefficients


## -description


Sets the coefficients for the equation used to composite the two input images.


## -parameters




### -param coefficients [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/6D931285-0F2B-44BE-8A1A-2348AC49A8DF">D2D1_VECTOR_4F</a></b>

The coefficients for the equation used to composite the two input images.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/06430DD6-B6BF-4F55-A99C-13860B800444">IDCompositionArithmeticCompositeEffect</a>
 

 

