---
UID: NF:dcomp.IDCompositionGaussianBlurEffect.SetStandardDeviation(float)
title: IDCompositionGaussianBlurEffect::SetStandardDeviation(float) (dcomp.h)
author: windows-sdk-content
description: Sets the amount of blur to be applied to the image.
old-location: directcomp\idcompositiongaussianblureffect_setstandarddeviation.htm
tech.root: directcomp
ms.assetid: 8C4BD86D-F15A-4F5C-9411-2C89A74E8370
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionGaussianBlurEffect interface [DirectComposition],SetStandardDeviation method, IDCompositionGaussianBlurEffect.SetStandardDeviation, IDCompositionGaussianBlurEffect.SetStandardDeviation(float), IDCompositionGaussianBlurEffect::SetStandardDeviation, IDCompositionGaussianBlurEffect::SetStandardDeviation(float), SetStandardDeviation, SetStandardDeviation method [DirectComposition], SetStandardDeviation method [DirectComposition],IDCompositionGaussianBlurEffect interface, dcomp/IDCompositionGaussianBlurEffect::SetStandardDeviation, directcomp.idcompositiongaussianblureffect_setstandarddeviation
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
 - IDCompositionGaussianBlurEffect.SetStandardDeviation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionGaussianBlurEffect::SetStandardDeviation(float)


## -description


Sets the amount of blur to be applied to the image.


## -parameters




### -param amount [in]

Type: <b>float</b>

The amount of blur to be applied to the image. You can compute the blur radius of the kernel by multiplying the standard deviation by 3.
            The units of both the standard deviation and blur radius are DIPs. A value of zero DIPs disables this effect entirely.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/CFE79B69-75EC-4E22-BC3E-C82601AE1213">IDCompositionGaussianBlurEffect</a>
 

 

