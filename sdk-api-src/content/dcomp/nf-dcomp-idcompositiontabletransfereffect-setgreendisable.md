---
UID: NF:dcomp.IDCompositionTableTransferEffect.SetGreenDisable
title: IDCompositionTableTransferEffect::SetGreenDisable (dcomp.h)
description: Specifies whether to apply the transfer function to the green channel.
helpviewer_keywords: ["IDCompositionTableTransferEffect interface [DirectComposition]","SetGreenDisable method","IDCompositionTableTransferEffect.SetGreenDisable","IDCompositionTableTransferEffect::SetGreenDisable","SetGreenDisable","SetGreenDisable method [DirectComposition]","SetGreenDisable method [DirectComposition]","IDCompositionTableTransferEffect interface","dcomp/IDCompositionTableTransferEffect::SetGreenDisable","directcomp.idcompositiontabletransfereffect_setgreendisable"]
old-location: directcomp\idcompositiontabletransfereffect_setgreendisable.htm
tech.root: directcomp
ms.assetid: C625ACED-C8E8-414D-A9E9-4119F8F1D434
ms.date: 12/05/2018
ms.keywords: IDCompositionTableTransferEffect interface [DirectComposition],SetGreenDisable method, IDCompositionTableTransferEffect.SetGreenDisable, IDCompositionTableTransferEffect::SetGreenDisable, SetGreenDisable, SetGreenDisable method [DirectComposition], SetGreenDisable method [DirectComposition],IDCompositionTableTransferEffect interface, dcomp/IDCompositionTableTransferEffect::SetGreenDisable, directcomp.idcompositiontabletransfereffect_setgreendisable
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
 - IDCompositionTableTransferEffect::SetGreenDisable
 - dcomp/IDCompositionTableTransferEffect::SetGreenDisable
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
 - IDCompositionTableTransferEffect.SetGreenDisable
---

# IDCompositionTableTransferEffect::SetGreenDisable


## -description

Specifies whether to apply the transfer function to the green channel.

## -parameters

### -param greenDisable [in]

Type: <b>BOOL</b>

A boolean value that specifies whether to apply the transfer function to the green channel.
            If you set this to TRUE the effect does not apply the transfer function to the green channel. If you set this to FALSE it applies the GreenTableTransfer function to the green channel.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontabletransfereffect">IDCompositionTableTransferEffect</a>