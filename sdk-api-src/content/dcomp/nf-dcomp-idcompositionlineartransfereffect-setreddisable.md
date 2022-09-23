---
UID: NF:dcomp.IDCompositionLinearTransferEffect.SetRedDisable
title: IDCompositionLinearTransferEffect::SetRedDisable (dcomp.h)
description: Specifies whether to apply the transfer function to the red channel. (IDCompositionLinearTransferEffect.SetRedDisable)
helpviewer_keywords: ["IDCompositionLinearTransferEffect interface [DirectComposition]","SetRedDisable method","IDCompositionLinearTransferEffect.SetRedDisable","IDCompositionLinearTransferEffect::SetRedDisable","SetRedDisable","SetRedDisable method [DirectComposition]","SetRedDisable method [DirectComposition]","IDCompositionLinearTransferEffect interface","dcomp/IDCompositionLinearTransferEffect::SetRedDisable","directcomp.idcompositionlineartransfereffect_setreddisable"]
old-location: directcomp\idcompositionlineartransfereffect_setreddisable.htm
tech.root: directcomp
ms.assetid: 59B82C2B-9DAE-4B6C-A5ED-425A8ACEF24E
ms.date: 12/05/2018
ms.keywords: IDCompositionLinearTransferEffect interface [DirectComposition],SetRedDisable method, IDCompositionLinearTransferEffect.SetRedDisable, IDCompositionLinearTransferEffect::SetRedDisable, SetRedDisable, SetRedDisable method [DirectComposition], SetRedDisable method [DirectComposition],IDCompositionLinearTransferEffect interface, dcomp/IDCompositionLinearTransferEffect::SetRedDisable, directcomp.idcompositionlineartransfereffect_setreddisable
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
 - IDCompositionLinearTransferEffect::SetRedDisable
 - dcomp/IDCompositionLinearTransferEffect::SetRedDisable
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
 - IDCompositionLinearTransferEffect.SetRedDisable
---

# IDCompositionLinearTransferEffect::SetRedDisable


## -description

Specifies whether to apply the transfer function to the red channel.

## -parameters

### -param redDisable [in]

Type: <b>BOOL</b>

A boolean value that specifies whether to apply the transfer function to the red channel.
            If you set this to TRUE the effect does not apply the transfer function to the red channel. If you set this to FALSE the effect applies the RedLinearTransfer function to the red channel.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionlineartransfereffect">IDCompositionLinearTransferEffect</a>
