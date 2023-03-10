---
UID: NF:dcomp.IDCompositionTurbulenceEffect.SetSize
title: IDCompositionTurbulenceEffect::SetSize (dcomp.h)
description: Sets the size of the turbulence output.
helpviewer_keywords: ["IDCompositionTurbulenceEffect interface [DirectComposition]","SetSize method","IDCompositionTurbulenceEffect.SetSize","IDCompositionTurbulenceEffect::SetSize","SetSize","SetSize method [DirectComposition]","SetSize method [DirectComposition]","IDCompositionTurbulenceEffect interface","dcomp/IDCompositionTurbulenceEffect::SetSize","directcomp.idcompositionturbulenceeffect_setsize"]
old-location: directcomp\idcompositionturbulenceeffect_setsize.htm
tech.root: directcomp
ms.assetid: A25788DC-83EE-455F-BC73-67639F47FFEC
ms.date: 12/05/2018
ms.keywords: IDCompositionTurbulenceEffect interface [DirectComposition],SetSize method, IDCompositionTurbulenceEffect.SetSize, IDCompositionTurbulenceEffect::SetSize, SetSize, SetSize method [DirectComposition], SetSize method [DirectComposition],IDCompositionTurbulenceEffect interface, dcomp/IDCompositionTurbulenceEffect::SetSize, directcomp.idcompositionturbulenceeffect_setsize
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
 - IDCompositionTurbulenceEffect::SetSize
 - dcomp/IDCompositionTurbulenceEffect::SetSize
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
 - IDCompositionTurbulenceEffect.SetSize
---

# IDCompositionTurbulenceEffect::SetSize


## -description

Sets the size of the turbulence output.

## -parameters

### -param size [in, ref]

Type: <b>const <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a></b>

The size of the turbulence output

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionturbulenceeffect">IDCompositionTurbulenceEffect</a>