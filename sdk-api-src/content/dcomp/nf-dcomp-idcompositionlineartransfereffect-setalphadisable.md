---
UID: NF:dcomp.IDCompositionLinearTransferEffect.SetAlphaDisable
title: IDCompositionLinearTransferEffect::SetAlphaDisable (dcomp.h)
description: Specifies whether to apply the transfer function to the alpha channel.
helpviewer_keywords: ["IDCompositionLinearTransferEffect interface [DirectComposition]","SetAlphaDisable method","IDCompositionLinearTransferEffect.SetAlphaDisable","IDCompositionLinearTransferEffect::SetAlphaDisable","SetAlphaDisable","SetAlphaDisable method [DirectComposition]","SetAlphaDisable method [DirectComposition]","IDCompositionLinearTransferEffect interface","dcomp/IDCompositionLinearTransferEffect::SetAlphaDisable","directcomp.idcompositionlineartransfereffect_setalphadisable"]
old-location: directcomp\idcompositionlineartransfereffect_setalphadisable.htm
tech.root: directcomp
ms.assetid: B0D76D35-FDB8-45CA-8D41-8D6C9597ED1B
ms.date: 12/05/2018
ms.keywords: IDCompositionLinearTransferEffect interface [DirectComposition],SetAlphaDisable method, IDCompositionLinearTransferEffect.SetAlphaDisable, IDCompositionLinearTransferEffect::SetAlphaDisable, SetAlphaDisable, SetAlphaDisable method [DirectComposition], SetAlphaDisable method [DirectComposition],IDCompositionLinearTransferEffect interface, dcomp/IDCompositionLinearTransferEffect::SetAlphaDisable, directcomp.idcompositionlineartransfereffect_setalphadisable
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
 - IDCompositionLinearTransferEffect::SetAlphaDisable
 - dcomp/IDCompositionLinearTransferEffect::SetAlphaDisable
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
 - IDCompositionLinearTransferEffect.SetAlphaDisable
---

# IDCompositionLinearTransferEffect::SetAlphaDisable


## -description

Specifies whether to apply the transfer function to the alpha channel.

## -parameters

### -param alphaDisable [in]

Type: <b>BOOL</b>

A boolean value that specifies whether to apply the transfer function to the alpha channel.
            If you set this to TRUE the effect does not apply the transfer function to the Alpha channel. If you set this to FALSE it applies the AlphaLinearTransfer function to the Alpha channel.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionlineartransfereffect">IDCompositionLinearTransferEffect</a>