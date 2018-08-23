---
UID: NF:dcomp.IDCompositionShadowEffect.SetStandardDeviation(IDCompositionAnimation)
title: IDCompositionShadowEffect::SetStandardDeviation(IDCompositionAnimation)
author: windows-sdk-content
description: Sets the amount of blur to be applied to the alpha channel of the image.
old-location: directcomp\idcompositionshadoweffect_setstandarddeviation.htm
old-project: directcomp
ms.assetid: 5860E4F6-D778-4F10-ACE1-416E6D378528
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionShadowEffect interface [DirectComposition],SetStandardDeviation method, IDCompositionShadowEffect.SetStandardDeviation, IDCompositionShadowEffect.SetStandardDeviation(IDCompositionAnimation), IDCompositionShadowEffect::SetStandardDeviation, IDCompositionShadowEffect::SetStandardDeviation(IDCompositionAnimation), SetStandardDeviation, SetStandardDeviation method [DirectComposition], SetStandardDeviation method [DirectComposition],IDCompositionShadowEffect interface, dcomp/IDCompositionShadowEffect::SetStandardDeviation, directcomp.idcompositionshadoweffect_setstandarddeviation
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
 - IDCompositionShadowEffect.SetStandardDeviation
product: Windows
targetos: Windows
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# IDCompositionShadowEffect::SetStandardDeviation(IDCompositionAnimation)


## -description


Sets the amount of blur to be applied to the alpha channel of the image.


## -parameters




### -param animation






#### - amount [in]

Type: <b>float</b>

The amount of blur to be applied to the alpha channel of the image. You can compute the blur radius of the kernel by multiplying the standard deviation by 3.
            The units of both the standard deviation and blur radius are DIPs.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/115FD667-64D2-4538-9EB4-B133D5DCAF30">IDCompositionShadowEffect</a>
 

 

