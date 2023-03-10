---
UID: NF:dcomp.IDCompositionBlendEffect.SetMode
title: IDCompositionBlendEffect::SetMode (dcomp.h)
description: Sets the blend mode to use when the blend effect combines the two images.
helpviewer_keywords: ["IDCompositionBlendEffect interface [DirectComposition]","SetMode method","IDCompositionBlendEffect.SetMode","IDCompositionBlendEffect::SetMode","SetMode","SetMode method [DirectComposition]","SetMode method [DirectComposition]","IDCompositionBlendEffect interface","dcomp/IDCompositionBlendEffect::SetMode","directcomp.idcompositionblendeffect_setmode"]
old-location: directcomp\idcompositionblendeffect_setmode.htm
tech.root: directcomp
ms.assetid: 61D64543-565B-4E64-B20E-03B1CD0F8FCA
ms.date: 12/05/2018
ms.keywords: IDCompositionBlendEffect interface [DirectComposition],SetMode method, IDCompositionBlendEffect.SetMode, IDCompositionBlendEffect::SetMode, SetMode, SetMode method [DirectComposition], SetMode method [DirectComposition],IDCompositionBlendEffect interface, dcomp/IDCompositionBlendEffect::SetMode, directcomp.idcompositionblendeffect_setmode
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
 - IDCompositionBlendEffect::SetMode
 - dcomp/IDCompositionBlendEffect::SetMode
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
 - IDCompositionBlendEffect.SetMode
---

# IDCompositionBlendEffect::SetMode


## -description

Sets the blend mode to use when the blend effect combines the two images.

## -parameters

### -param mode [in]

Type: <b><a href="/windows/desktop/Direct2D/blend">D2D1_BLEND_MODE</a></b>

The blend mode to use when the blend effect combines the two images.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionblendeffect">IDCompositionBlendEffect</a>