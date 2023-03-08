---
UID: NF:dcomp.IDCompositionLinearTransferEffect.SetClampOutput
title: IDCompositionLinearTransferEffect::SetClampOutput (dcomp.h)
description: The IDCompositionLinearTransferEffect::SetClampOutput method specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.
helpviewer_keywords: ["IDCompositionLinearTransferEffect interface [DirectComposition]","SetClampOutput method","IDCompositionLinearTransferEffect.SetClampOutput","IDCompositionLinearTransferEffect::SetClampOutput","SetClampOutput","SetClampOutput method [DirectComposition]","SetClampOutput method [DirectComposition]","IDCompositionLinearTransferEffect interface","dcomp/IDCompositionLinearTransferEffect::SetClampOutput","directcomp.idcompositionlineartransfereffect_setclampoutput"]
old-location: directcomp\idcompositionlineartransfereffect_setclampoutput.htm
tech.root: directcomp
ms.assetid: D56B3B15-6437-46A3-B1F9-88F5BC4A9BB2
ms.date: 06/23/2022
ms.keywords: IDCompositionLinearTransferEffect interface [DirectComposition],SetClampOutput method, IDCompositionLinearTransferEffect.SetClampOutput, IDCompositionLinearTransferEffect::SetClampOutput, SetClampOutput, SetClampOutput method [DirectComposition], SetClampOutput method [DirectComposition],IDCompositionLinearTransferEffect interface, dcomp/IDCompositionLinearTransferEffect::SetClampOutput, directcomp.idcompositionlineartransfereffect_setclampoutput
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
 - IDCompositionLinearTransferEffect::SetClampOutput
 - dcomp/IDCompositionLinearTransferEffect::SetClampOutput
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
 - IDCompositionLinearTransferEffect.SetClampOutput
---

# IDCompositionLinearTransferEffect::SetClampOutput


## -description

Specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.

## -parameters

### -param clampOutput [in]

Type: <b>BOOL</b>

A boolean value that specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.
            If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values, but other effects and the output
            surface may clamp the values if they are not of high enough precision.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionlineartransfereffect">IDCompositionLinearTransferEffect</a>