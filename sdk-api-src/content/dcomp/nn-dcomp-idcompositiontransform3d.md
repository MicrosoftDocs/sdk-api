---
UID: NN:dcomp.IDCompositionTransform3D
title: IDCompositionTransform3D (dcomp.h)
description: Represents a 3D transformation effect that can be used to modify the rasterization of a visual subtree.
helpviewer_keywords: ["IDCompositionTransform3D","IDCompositionTransform3D interface [DirectComposition]","IDCompositionTransform3D interface [DirectComposition]","described","dcomp/IDCompositionTransform3D","directcomp.idcompositiontransform3d"]
old-location: directcomp\idcompositiontransform3d.htm
tech.root: directcomp
ms.assetid: 81239AB4-C2A3-4E37-95E3-B3C10532EE15
ms.date: 12/05/2018
ms.keywords: IDCompositionTransform3D, IDCompositionTransform3D interface [DirectComposition], IDCompositionTransform3D interface [DirectComposition],described, dcomp/IDCompositionTransform3D, directcomp.idcompositiontransform3d
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionTransform3D
 - dcomp/IDCompositionTransform3D
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
 - IDCompositionTransform3D
---

# IDCompositionTransform3D interface


## -description

Represents a 3D transformation effect that can be used to modify the rasterization of a visual subtree.

## -remarks

The <b>IDCompositionTransform3D</b> interface is an abstract interface that represents a 3D perspective transformation effect. A 3D transform object can be associated with multiple visuals and multiple effect groups. When a 3D transform object is modified, all affected visuals are recomposed to reflect the change.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffect">IDCompositionEffect</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>