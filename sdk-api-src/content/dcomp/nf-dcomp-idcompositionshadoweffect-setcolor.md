---
UID: NF:dcomp.IDCompositionShadowEffect.SetColor
title: IDCompositionShadowEffect::SetColor (dcomp.h)
description: Sets color of the shadow.
helpviewer_keywords: ["IDCompositionShadowEffect interface [DirectComposition]","SetColor method","IDCompositionShadowEffect.SetColor","IDCompositionShadowEffect::SetColor","SetColor","SetColor method [DirectComposition]","SetColor method [DirectComposition]","IDCompositionShadowEffect interface","dcomp/IDCompositionShadowEffect::SetColor","directcomp.idcompositionshadoweffect_setcolor"]
old-location: directcomp\idcompositionshadoweffect_setcolor.htm
tech.root: directcomp
ms.assetid: 1C08E464-087A-41BF-9B0E-E1370576E64A
ms.date: 12/05/2018
ms.keywords: IDCompositionShadowEffect interface [DirectComposition],SetColor method, IDCompositionShadowEffect.SetColor, IDCompositionShadowEffect::SetColor, SetColor, SetColor method [DirectComposition], SetColor method [DirectComposition],IDCompositionShadowEffect interface, dcomp/IDCompositionShadowEffect::SetColor, directcomp.idcompositionshadoweffect_setcolor
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
 - IDCompositionShadowEffect::SetColor
 - dcomp/IDCompositionShadowEffect::SetColor
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
 - IDCompositionShadowEffect.SetColor
---

# IDCompositionShadowEffect::SetColor


## -description

Sets color of the shadow.

## -parameters

### -param color [in, ref]

Type: <b>const <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f">D2D1_VECTOR_4F</a></b>

The color of the shadow.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionshadoweffect">IDCompositionShadowEffect</a>