---
UID: NF:dcomp.IDCompositionCompositeEffect.SetMode
title: IDCompositionCompositeEffect::SetMode (dcomp.h)
description: Sets the mode for the composite effect.
helpviewer_keywords: ["IDCompositionCompositeEffect interface [DirectComposition]","SetMode method","IDCompositionCompositeEffect.SetMode","IDCompositionCompositeEffect::SetMode","SetMode","SetMode method [DirectComposition]","SetMode method [DirectComposition]","IDCompositionCompositeEffect interface","dcomp/IDCompositionCompositeEffect::SetMode","directcomp.idcompositioncompositeeffect_setmode"]
old-location: directcomp\idcompositioncompositeeffect_setmode.htm
tech.root: directcomp
ms.assetid: E93FAAA1-A9C3-466A-9023-99745EA6A49B
ms.date: 12/05/2018
ms.keywords: IDCompositionCompositeEffect interface [DirectComposition],SetMode method, IDCompositionCompositeEffect.SetMode, IDCompositionCompositeEffect::SetMode, SetMode, SetMode method [DirectComposition], SetMode method [DirectComposition],IDCompositionCompositeEffect interface, dcomp/IDCompositionCompositeEffect::SetMode, directcomp.idcompositioncompositeeffect_setmode
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
 - IDCompositionCompositeEffect::SetMode
 - dcomp/IDCompositionCompositeEffect::SetMode
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
 - IDCompositionCompositeEffect.SetMode
---

# IDCompositionCompositeEffect::SetMode


## -description

Sets the mode for the composite effect.

## -parameters

### -param mode [in]

Type: <b><a href="/windows/desktop/Direct2D/composite">D2D1_COMPOSITE_MODE</a></b>

The mode for the composite effect.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioncompositeeffect">IDCompositionCompositeEffect</a>