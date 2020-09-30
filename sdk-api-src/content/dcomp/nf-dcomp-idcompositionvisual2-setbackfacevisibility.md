---
UID: NF:dcomp.IDCompositionVisual2.SetBackFaceVisibility
title: IDCompositionVisual2::SetBackFaceVisibility (dcomp.h)
description: Specifies whether or not surfaces that have 3D transformations applied to them should be displayed when facing away from the observer.
helpviewer_keywords: ["IDCompositionVisual2 interface [DirectComposition]","SetBackFaceVisibility method","IDCompositionVisual2.SetBackFaceVisibility","IDCompositionVisual2::SetBackFaceVisibility","SetBackFaceVisibility","SetBackFaceVisibility method [DirectComposition]","SetBackFaceVisibility method [DirectComposition]","IDCompositionVisual2 interface","dcomp/IDCompositionVisual2::SetBackFaceVisibility","directcomp.idcompositionvisual2_setbackfacevisibility"]
old-location: directcomp\idcompositionvisual2_setbackfacevisibility.htm
tech.root: directcomp
ms.assetid: A488A0B9-3CBE-477A-9688-84A7DA43D7F6
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual2 interface [DirectComposition],SetBackFaceVisibility method, IDCompositionVisual2.SetBackFaceVisibility, IDCompositionVisual2::SetBackFaceVisibility, SetBackFaceVisibility, SetBackFaceVisibility method [DirectComposition], SetBackFaceVisibility method [DirectComposition],IDCompositionVisual2 interface, dcomp/IDCompositionVisual2::SetBackFaceVisibility, directcomp.idcompositionvisual2_setbackfacevisibility
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDCompositionVisual2::SetBackFaceVisibility
 - dcomp/IDCompositionVisual2::SetBackFaceVisibility
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
 - IDCompositionVisual2.SetBackFaceVisibility
---

## -description

Specifies whether or not surfaces that have 3D transformations applied to them should be displayed when facing away from the observer.

## -parameters

### -param visibility

[in]

The back face visibility to use when composing surfaces in this visual’s sub-tree to the screen.

## -returns

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

The back face visibility property affects how surfaces that have 3D transformations applied are rendered.

By default, a visual inherits the back face visibility property of its parent visual, which may inherit the back face visibility property of its parent visual, and so on. A visual uses the DCOMPOSITION_BACKFACE_VISIBILITY_VISIBLE mode if this method is never called for the visual, or if this method is called with DCOMPOSITION_BACKFACE_VISIBILITY_INHERIT. If no visuals set the back face visibility property, the default for the entire visual tree is DCOMPOSITION_BACKFACE_VISIBILITY_VISIBLE. 

If the <i>visibility</i> parameter is anything other than DCOMPOSITION_BACKFACE_VISIBILITY_INHERIT, this visual's surfaces are composed with the specified visibility mode. In addition, this visibility mode becomes the new default for the children of the current visual. That is, if the visibility mode of this visual's children is unchanged or explicitly set to DCOMPOSITION_BACKFACE_VISIBILITY_INHERIT, the surfaces the child visuals are composed using the visibility mode of this visual.

## -see-also

<a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DCompV2BackfaceandD2DBatching">DirectComposition Backface and D2D Batching</a>

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d">IDCompositionEffectGroup::SetTransform3D</a>

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual2">IDCompositionVisual2</a>