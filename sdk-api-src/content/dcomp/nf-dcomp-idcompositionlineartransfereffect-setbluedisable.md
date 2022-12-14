---
UID: NF:dcomp.IDCompositionLinearTransferEffect.SetBlueDisable
title: IDCompositionLinearTransferEffect::SetBlueDisable (dcomp.h)
description: The IDCompositionLinearTransferEffect::SetBlueDisable method specifies whether to apply the transfer function to the blue channel.
helpviewer_keywords: ["IDCompositionLinearTransferEffect interface [DirectComposition]","SetBlueDisable method","IDCompositionLinearTransferEffect.SetBlueDisable","IDCompositionLinearTransferEffect::SetBlueDisable","SetBlueDisable","SetBlueDisable method [DirectComposition]","SetBlueDisable method [DirectComposition]","IDCompositionLinearTransferEffect interface","dcomp/IDCompositionLinearTransferEffect::SetBlueDisable","directcomp.idcompositionlineartransfereffect_setbluedisable"]
old-location: directcomp\idcompositionlineartransfereffect_setbluedisable.htm
tech.root: directcomp
ms.assetid: DE87E53B-4469-4B30-8397-6A0712DE8A6C
ms.date: 06/23/2022
ms.keywords: IDCompositionLinearTransferEffect interface [DirectComposition],SetBlueDisable method, IDCompositionLinearTransferEffect.SetBlueDisable, IDCompositionLinearTransferEffect::SetBlueDisable, SetBlueDisable, SetBlueDisable method [DirectComposition], SetBlueDisable method [DirectComposition],IDCompositionLinearTransferEffect interface, dcomp/IDCompositionLinearTransferEffect::SetBlueDisable, directcomp.idcompositionlineartransfereffect_setbluedisable
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
 - IDCompositionLinearTransferEffect::SetBlueDisable
 - dcomp/IDCompositionLinearTransferEffect::SetBlueDisable
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
 - IDCompositionLinearTransferEffect.SetBlueDisable
---

# IDCompositionLinearTransferEffect::SetBlueDisable


## -description

Specifies whether to apply the transfer function to the blue channel.

## -parameters

### -param blueDisable [in]

Type: <b>BOOL</b>

A boolean value that specifies whether to apply the transfer function to the blue channel.
            If you set this to TRUE the effect does not apply the transfer function to the blue channel. If you set this to FALSE it applies the BlueLinearTransfer function to the blue channel.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionlineartransfereffect">IDCompositionLinearTransferEffect</a>