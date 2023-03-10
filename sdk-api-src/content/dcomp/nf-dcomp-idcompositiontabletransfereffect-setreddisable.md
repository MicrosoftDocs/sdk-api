---
UID: NF:dcomp.IDCompositionTableTransferEffect.SetRedDisable
title: IDCompositionTableTransferEffect::SetRedDisable (dcomp.h)
description: Specifies whether to apply the transfer function to the red channel. (IDCompositionTableTransferEffect.SetRedDisable)
helpviewer_keywords: ["IDCompositionTableTransferEffect interface [DirectComposition]","SetRedDisable method","IDCompositionTableTransferEffect.SetRedDisable","IDCompositionTableTransferEffect::SetRedDisable","SetRedDisable","SetRedDisable method [DirectComposition]","SetRedDisable method [DirectComposition]","IDCompositionTableTransferEffect interface","dcomp/IDCompositionTableTransferEffect::SetRedDisable","directcomp.idcompositiontabletransfereffect_setreddisable"]
old-location: directcomp\idcompositiontabletransfereffect_setreddisable.htm
tech.root: directcomp
ms.assetid: 9CDE9200-F5AF-47AB-9B79-8602188FF4CA
ms.date: 12/05/2018
ms.keywords: IDCompositionTableTransferEffect interface [DirectComposition],SetRedDisable method, IDCompositionTableTransferEffect.SetRedDisable, IDCompositionTableTransferEffect::SetRedDisable, SetRedDisable, SetRedDisable method [DirectComposition], SetRedDisable method [DirectComposition],IDCompositionTableTransferEffect interface, dcomp/IDCompositionTableTransferEffect::SetRedDisable, directcomp.idcompositiontabletransfereffect_setreddisable
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
 - IDCompositionTableTransferEffect::SetRedDisable
 - dcomp/IDCompositionTableTransferEffect::SetRedDisable
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
 - IDCompositionTableTransferEffect.SetRedDisable
---

# IDCompositionTableTransferEffect::SetRedDisable


## -description

Specifies whether to apply the transfer function to the red channel.

## -parameters

### -param redDisable [in]

Type: <b>BOOL</b>

A boolean value that specifies whether to apply the transfer function to the red channel.
            If you set this to TRUE the effect does not apply the transfer function to the red channel. If you set this to FALSE it applies the RedTableTransfer function to the red channel.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontabletransfereffect">IDCompositionTableTransferEffect</a>
