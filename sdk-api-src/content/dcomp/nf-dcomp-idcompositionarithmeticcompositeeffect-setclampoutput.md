---
UID: NF:dcomp.IDCompositionArithmeticCompositeEffect.SetClampOutput
title: IDCompositionArithmeticCompositeEffect::SetClampOutput (dcomp.h)
description: Specifies whether to clamp color values before the effect passes the values to the next effect in the graph.
helpviewer_keywords: ["IDCompositionArithmeticCompositeEffect interface [DirectComposition]","SetClampOutput method","IDCompositionArithmeticCompositeEffect.SetClampOutput","IDCompositionArithmeticCompositeEffect::SetClampOutput","SetClampOutput","SetClampOutput method [DirectComposition]","SetClampOutput method [DirectComposition]","IDCompositionArithmeticCompositeEffect interface","dcomp/IDCompositionArithmeticCompositeEffect::SetClampOutput","directcomp.idcompositionarithmeticcompositeeffect_setclampoutput"]
old-location: directcomp\idcompositionarithmeticcompositeeffect_setclampoutput.htm
tech.root: directcomp
ms.assetid: 6558E6E7-FEF3-43F0-8508-197BA1DE3D10
ms.date: 12/05/2018
ms.keywords: IDCompositionArithmeticCompositeEffect interface [DirectComposition],SetClampOutput method, IDCompositionArithmeticCompositeEffect.SetClampOutput, IDCompositionArithmeticCompositeEffect::SetClampOutput, SetClampOutput, SetClampOutput method [DirectComposition], SetClampOutput method [DirectComposition],IDCompositionArithmeticCompositeEffect interface, dcomp/IDCompositionArithmeticCompositeEffect::SetClampOutput, directcomp.idcompositionarithmeticcompositeeffect_setclampoutput
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
 - IDCompositionArithmeticCompositeEffect::SetClampOutput
 - dcomp/IDCompositionArithmeticCompositeEffect::SetClampOutput
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
 - IDCompositionArithmeticCompositeEffect.SetClampOutput
---

# IDCompositionArithmeticCompositeEffect::SetClampOutput


## -description

Specifies whether to clamp color values before the effect passes the values to the next effect in the graph.

## -parameters

### -param clampoutput [in]

Type: <b>BOOL</b>

A boolean value indicating whether to clamp the color values.  A value of TRUE causes color values to be clamped between 0 and 1.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionarithmeticcompositeeffect">IDCompositionArithmeticCompositeEffect</a>