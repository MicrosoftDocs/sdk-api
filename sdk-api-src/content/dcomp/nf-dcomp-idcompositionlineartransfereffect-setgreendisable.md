---
UID: NF:dcomp.IDCompositionLinearTransferEffect.SetGreenDisable
title: IDCompositionLinearTransferEffect::SetGreenDisable (dcomp.h)
description: The IDCompositionLinearTransferEffect::SetGreenDisable method specifies whether to apply the transfer function to the green channel.
helpviewer_keywords: ["IDCompositionLinearTransferEffect interface [DirectComposition]","SetGreenDisable method","IDCompositionLinearTransferEffect.SetGreenDisable","IDCompositionLinearTransferEffect::SetGreenDisable","SetGreenDisable","SetGreenDisable method [DirectComposition]","SetGreenDisable method [DirectComposition]","IDCompositionLinearTransferEffect interface","dcomp/IDCompositionLinearTransferEffect::SetGreenDisable","directcomp.idcompositionlineartransfereffect_setgreendisable"]
old-location: directcomp\idcompositionlineartransfereffect_setgreendisable.htm
tech.root: directcomp
ms.assetid: 5C0C9E9C-F332-4F4E-A3F0-423A302AC6FC
ms.date: 06/23/2022
ms.keywords: IDCompositionLinearTransferEffect interface [DirectComposition],SetGreenDisable method, IDCompositionLinearTransferEffect.SetGreenDisable, IDCompositionLinearTransferEffect::SetGreenDisable, SetGreenDisable, SetGreenDisable method [DirectComposition], SetGreenDisable method [DirectComposition],IDCompositionLinearTransferEffect interface, dcomp/IDCompositionLinearTransferEffect::SetGreenDisable, directcomp.idcompositionlineartransfereffect_setgreendisable
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
 - IDCompositionLinearTransferEffect::SetGreenDisable
 - dcomp/IDCompositionLinearTransferEffect::SetGreenDisable
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
 - IDCompositionLinearTransferEffect.SetGreenDisable
---

# IDCompositionLinearTransferEffect::SetGreenDisable


## -description

Specifies whether to apply the transfer function to the green channel.

## -parameters

### -param greenDisable [in]

Type: <b>BOOL</b>

A boolean value that specifies whether to apply the transfer function to the green channel.
            If you set this to TRUE the effect does not apply the transfer function to the green channel. If you set this to FALSE it applies the GreenLinearTransfer function to the green channel.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionlineartransfereffect">IDCompositionLinearTransferEffect</a>