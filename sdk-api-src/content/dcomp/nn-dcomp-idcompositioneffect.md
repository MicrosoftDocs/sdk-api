---
UID: NN:dcomp.IDCompositionEffect
title: IDCompositionEffect (dcomp.h)
description: Represents a bitmap effect that modifies the rasterization of a visual's subtree.helpviewer_keywords: ["IDCompositionEffect","IDCompositionEffect interface [DirectComposition]","IDCompositionEffect interface [DirectComposition]","described","dcomp/IDCompositionEffect","directcomp.idcompositioneffect"]
old-location: directcomp\idcompositioneffect.htm
tech.root: directcomp
ms.assetid: 9C9DFECD-0EC0-446C-8CCC-BB7979B01575
ms.date: 12/05/2018
ms.keywords: IDCompositionEffect, IDCompositionEffect interface [DirectComposition], IDCompositionEffect interface [DirectComposition],described, dcomp/IDCompositionEffect, directcomp.idcompositioneffect
f1_keywords:
- dcomp/IDCompositionEffect
dev_langs:
- c++
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- IDCompositionEffect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionEffect interface


## -description


Represents a bitmap effect that modifies the rasterization of a visual's subtree.




## -remarks



<b>IDCompositionEffect</b> is an abstract interface that represents a bitmap effect. An effect applies to the entire visual subtree rooted at the visual that the effect is associated with. An effect object can be associated with multiple visuals. When an effect object is modified, all affected visuals are recomposed to reflect the change.



More than one effect can be simultaneously applied to a visual by using the <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffectgroup">IDCompositionEffectGroup</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>
 

 

