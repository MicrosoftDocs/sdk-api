---
UID: NF:dcomp.IDCompositionArithmeticCompositeEffect.SetCoefficient3(IDCompositionAnimation)
title: IDCompositionArithmeticCompositeEffect::SetCoefficient3(IDCompositionAnimation) (dcomp.h)
author: windows-sdk-content
description: Sets the third coefficient for the equation used to composite the two input images.
old-location: directcomp\idcompositionarithmeticcompositeeffect_setcoefficient3_2.htm
tech.root: directcomp
ms.assetid: C08978C7-7028-4E48-B19F-1FC682E0FB82
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionArithmeticCompositeEffect interface [DirectComposition],SetCoefficient3 method, IDCompositionArithmeticCompositeEffect.SetCoefficient3, IDCompositionArithmeticCompositeEffect.SetCoefficient3(IDCompositionAnimation), IDCompositionArithmeticCompositeEffect::SetCoefficient3, IDCompositionArithmeticCompositeEffect::SetCoefficient3(IDCompositionAnimation), SetCoefficient3, SetCoefficient3 method [DirectComposition], SetCoefficient3 method [DirectComposition],IDCompositionArithmeticCompositeEffect interface, dcomp/IDCompositionArithmeticCompositeEffect::SetCoefficient3, directcomp.idcompositionarithmeticcompositeeffect_setcoefficient3_2
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
 - IDCompositionArithmeticCompositeEffect.SetCoefficient3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionArithmeticCompositeEffect::SetCoefficient3(IDCompositionAnimation)


## -description


Sets the third coefficient for the equation used to composite the two input images.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation that represents how the value of the third coefficient changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/06430DD6-B6BF-4F55-A99C-13860B800444">IDCompositionArithmeticCompositeEffect</a>
 

 

