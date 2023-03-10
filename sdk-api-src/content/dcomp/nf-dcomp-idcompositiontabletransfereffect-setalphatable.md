---
UID: NF:dcomp.IDCompositionTableTransferEffect.SetAlphaTable
title: IDCompositionTableTransferEffect::SetAlphaTable (dcomp.h)
description: Sets the list of values used to define the transfer function for the alpha channel.
helpviewer_keywords: ["IDCompositionTableTransferEffect interface [DirectComposition]","SetAlphaTable method","IDCompositionTableTransferEffect.SetAlphaTable","IDCompositionTableTransferEffect::SetAlphaTable","SetAlphaTable","SetAlphaTable method [DirectComposition]","SetAlphaTable method [DirectComposition]","IDCompositionTableTransferEffect interface","dcomp/IDCompositionTableTransferEffect::SetAlphaTable","directcomp.idcompositiontabletransfereffect_setalphatable"]
old-location: directcomp\idcompositiontabletransfereffect_setalphatable.htm
tech.root: directcomp
ms.assetid: 8CF6673B-9D9C-40B9-AC91-B2F63450FE64
ms.date: 12/05/2018
ms.keywords: IDCompositionTableTransferEffect interface [DirectComposition],SetAlphaTable method, IDCompositionTableTransferEffect.SetAlphaTable, IDCompositionTableTransferEffect::SetAlphaTable, SetAlphaTable, SetAlphaTable method [DirectComposition], SetAlphaTable method [DirectComposition],IDCompositionTableTransferEffect interface, dcomp/IDCompositionTableTransferEffect::SetAlphaTable, directcomp.idcompositiontabletransfereffect_setalphatable
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
 - IDCompositionTableTransferEffect::SetAlphaTable
 - dcomp/IDCompositionTableTransferEffect::SetAlphaTable
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
 - IDCompositionTableTransferEffect.SetAlphaTable
---

# IDCompositionTableTransferEffect::SetAlphaTable


## -description

Sets the list of values used to define the transfer function for the alpha channel.

## -parameters

### -param tableValues [in]

Type: <b>const float*</b>

The list of values used to define the transfer function for the alpha channel.

### -param count [in]

Type: <b>UINT</b>

The number of values in the tableValues parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontabletransfereffect">IDCompositionTableTransferEffect</a>