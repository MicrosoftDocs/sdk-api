---
UID: NF:dcomp.IDCompositionShadowEffect.SetStandardDeviation(IDCompositionAnimation)
title: IDCompositionShadowEffect::SetStandardDeviation(IDCompositionAnimation)
author: windows-sdk-content
description: Sets the amount of blur to be applied to the alpha channel of the image.
old-location: directcomp\idcompositionshadoweffect_setstandarddeviation_2.htm
tech.root: directcomp
ms.assetid: B5470CF6-A24B-4168-904E-2465372B60FC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionShadowEffect interface [DirectComposition],SetStandardDeviation method, IDCompositionShadowEffect.SetStandardDeviation, IDCompositionShadowEffect.SetStandardDeviation(IDCompositionAnimation), IDCompositionShadowEffect::SetStandardDeviation, IDCompositionShadowEffect::SetStandardDeviation(IDCompositionAnimation), SetStandardDeviation, SetStandardDeviation method [DirectComposition], SetStandardDeviation method [DirectComposition],IDCompositionShadowEffect interface, dcomp/IDCompositionShadowEffect::SetStandardDeviation, directcomp.idcompositionshadoweffect_setstandarddeviation_2
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
 - IDCompositionShadowEffect.SetStandardDeviation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionShadowEffect::SetStandardDeviation(IDCompositionAnimation)


## -description


Sets the amount of blur to be applied to the alpha channel of the image.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation that represents how the amount of blur to be applied to the alpha channel of the image changes over time. 
            You can compute the blur radius of the kernel by multiplying the standard deviation by 3.
            The units of both the standard deviation and blur radius are DIPs.          
          This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn919766(v=VS.85).aspx">IDCompositionShadowEffect</a>
 

 

