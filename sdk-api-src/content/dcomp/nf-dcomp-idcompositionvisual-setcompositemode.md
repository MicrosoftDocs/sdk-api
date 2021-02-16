---
UID: NF:dcomp.IDCompositionVisual.SetCompositeMode
title: IDCompositionVisual::SetCompositeMode (dcomp.h)
description: Sets the blending mode for this visual.
helpviewer_keywords: ["IDCompositionVisual interface [DirectComposition]","SetCompositeMode method","IDCompositionVisual.SetCompositeMode","IDCompositionVisual::SetCompositeMode","SetCompositeMode","SetCompositeMode method [DirectComposition]","SetCompositeMode method [DirectComposition]","IDCompositionVisual interface","dcomp/IDCompositionVisual::SetCompositeMode","directcomp.idcompositionvisual_setcompositemode"]
old-location: directcomp\idcompositionvisual_setcompositemode.htm
tech.root: directcomp
ms.assetid: 2F8C7930-6BBC-4CA9-86C0-168BF0F9C0BD
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetCompositeMode method, IDCompositionVisual.SetCompositeMode, IDCompositionVisual::SetCompositeMode, SetCompositeMode, SetCompositeMode method [DirectComposition], SetCompositeMode method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetCompositeMode, directcomp.idcompositionvisual_setcompositemode
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
 - IDCompositionVisual::SetCompositeMode
 - dcomp/IDCompositionVisual::SetCompositeMode
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
 - IDCompositionVisual.SetCompositeMode
---

# IDCompositionVisual::SetCompositeMode


## -description

Sets the blending mode for this visual.

## -parameters

### -param compositeMode [in]

Type: <b><a href="/windows/desktop/api/dcomptypes/ne-dcomptypes-dcomposition_composite_mode">DCOMPOSITION_COMPOSITE_MODE</a></b>

The blending mode to use when composing the visual to the screen.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

The composite mode determines how visual's bitmap is blended with the screen. By default, the visual is blended with "source over" semantics; that is, the colors are blended with per-pixel transparency.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffectgroup">IDCompositionEffectGroup</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>