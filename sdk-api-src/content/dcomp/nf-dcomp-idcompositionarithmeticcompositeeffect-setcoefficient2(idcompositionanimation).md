---
UID: NF:dcomp.IDCompositionArithmeticCompositeEffect.SetCoefficient2(IDCompositionAnimation)
title: IDCompositionArithmeticCompositeEffect::SetCoefficient2(IDCompositionAnimation)
author: windows-sdk-content
description: Sets the second coefficient for the equation used to composite the two input images.
old-location: directcomp\idcompositionarithmeticcompositeeffect_setcoefficient2_2.htm
tech.root: directcomp
ms.assetid: C1A43316-58FA-4F42-827D-AF11104F5E60
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDCompositionArithmeticCompositeEffect interface [DirectComposition],SetCoefficient2 method, IDCompositionArithmeticCompositeEffect.SetCoefficient2, IDCompositionArithmeticCompositeEffect.SetCoefficient2(IDCompositionAnimation), IDCompositionArithmeticCompositeEffect::SetCoefficient2, IDCompositionArithmeticCompositeEffect::SetCoefficient2(IDCompositionAnimation), SetCoefficient2, SetCoefficient2 method [DirectComposition], SetCoefficient2 method [DirectComposition],IDCompositionArithmeticCompositeEffect interface, dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficient2, directcomp.idcompositionarithmeticcompositeeffect_setcoefficient2_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionArithmeticCompositeEffect::SetCoefficient2(IDCompositionAnimation)


## -description


Sets the second coefficient for the equation used to composite the two input images.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation that represents how the value of the second coefficient changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/06430DD6-B6BF-4F55-A99C-13860B800444">IDCompositionArithmeticCompositeEffect</a>
 

 

