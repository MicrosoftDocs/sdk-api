---
UID: NF:dcomp.IDCompositionTableTransferEffect.SetClampOutput
title: IDCompositionTableTransferEffect::SetClampOutput (dcomp.h)
description: Specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.
helpviewer_keywords: ["IDCompositionTableTransferEffect interface [DirectComposition]","SetClampOutput method","IDCompositionTableTransferEffect.SetClampOutput","IDCompositionTableTransferEffect::SetClampOutput","SetClampOutput","SetClampOutput method [DirectComposition]","SetClampOutput method [DirectComposition]","IDCompositionTableTransferEffect interface","dcomp/IDCompositionTableTransferEffect::SetClampOutput","directcomp.idcompositiontabletransfereffect_setclampoutput"]
old-location: directcomp\idcompositiontabletransfereffect_setclampoutput.htm
tech.root: directcomp
ms.assetid: 6F1A7757-92DA-4BDC-9894-7A8906461FD5
ms.date: 12/05/2018
ms.keywords: IDCompositionTableTransferEffect interface [DirectComposition],SetClampOutput method, IDCompositionTableTransferEffect.SetClampOutput, IDCompositionTableTransferEffect::SetClampOutput, SetClampOutput, SetClampOutput method [DirectComposition], SetClampOutput method [DirectComposition],IDCompositionTableTransferEffect interface, dcomp/IDCompositionTableTransferEffect::SetClampOutput, directcomp.idcompositiontabletransfereffect_setclampoutput
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
 - IDCompositionTableTransferEffect::SetClampOutput
 - dcomp/IDCompositionTableTransferEffect::SetClampOutput
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
 - IDCompositionTableTransferEffect.SetClampOutput
---

# IDCompositionTableTransferEffect::SetClampOutput


## -description

Specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.

## -parameters

### -param clampOutput [in]

Type: <b>BOOL</b>

A boolean value that specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.
            If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values,
            but other effects and the output surface may clamp the values if they are not of high enough precision.
            The effect clamps the values before it premultiplies the alpha.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontabletransfereffect">IDCompositionTableTransferEffect</a>