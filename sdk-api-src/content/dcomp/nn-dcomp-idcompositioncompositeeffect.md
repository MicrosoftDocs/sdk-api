---
UID: NN:dcomp.IDCompositionCompositeEffect
title: IDCompositionCompositeEffect (dcomp.h)
description: The composite effect is used to combine 2 or more images.
helpviewer_keywords: ["IDCompositionCompositeEffect","IDCompositionCompositeEffect interface [DirectComposition]","IDCompositionCompositeEffect interface [DirectComposition]","described","dcomp/IDCompositionCompositeEffect","directcomp.idcompositioncompositeeffect"]
old-location: directcomp\idcompositioncompositeeffect.htm
tech.root: directcomp
ms.assetid: 72647FCE-F1B0-4A50-927B-23EE38EEEC8B
ms.date: 12/05/2018
ms.keywords: IDCompositionCompositeEffect, IDCompositionCompositeEffect interface [DirectComposition], IDCompositionCompositeEffect interface [DirectComposition],described, dcomp/IDCompositionCompositeEffect, directcomp.idcompositioncompositeeffect
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionCompositeEffect
 - dcomp/IDCompositionCompositeEffect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionCompositeEffect
---

# IDCompositionCompositeEffect interface


## -description

The composite effect is used to combine 2 or more images. This effect has 13 different composite modes.
          The composite effect accepts 2 or more inputs. When you specify 2 images, destination is the first input (index 0) and the source is the second input (index 1). 
          If you specify more than 2 inputs, the images are composited starting with the first input and the second and so on.

## -inheritance

The <b>IDCompositionCompositeEffect</b> interface inherits from <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>. <b>IDCompositionCompositeEffect</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionfiltereffect">IDCompositionFilterEffect</a>
