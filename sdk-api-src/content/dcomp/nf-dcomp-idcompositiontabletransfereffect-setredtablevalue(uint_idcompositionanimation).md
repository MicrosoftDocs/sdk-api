---
UID: NF:dcomp.IDCompositionTableTransferEffect.SetRedTableValue(UINT,IDCompositionAnimation)
title: IDCompositionTableTransferEffect::SetRedTableValue(UINT,IDCompositionAnimation) (dcomp.h)
description: Sets a value in the red table. (overload 2/2)
helpviewer_keywords: ["IDCompositionTableTransferEffect interface [DirectComposition]","SetRedTableValue method","IDCompositionTableTransferEffect.SetRedTableValue","IDCompositionTableTransferEffect.SetRedTableValue(UINT","IDCompositionAnimation)","IDCompositionTableTransferEffect::SetRedTableValue","IDCompositionTableTransferEffect::SetRedTableValue(UINT","IDCompositionAnimation)","SetRedTableValue","SetRedTableValue method [DirectComposition]","SetRedTableValue method [DirectComposition]","IDCompositionTableTransferEffect interface","dcomp/IDCompositionTableTransferEffect::SetRedTableValue","directcomp.idcompositiontabletransfereffect_setredtablevalue_2"]
old-location: directcomp\idcompositiontabletransfereffect_setredtablevalue_2.htm
tech.root: directcomp
ms.assetid: 983E302A-F13C-48A7-9C9F-9569EB4585D3
ms.date: 12/05/2018
ms.keywords: IDCompositionTableTransferEffect interface [DirectComposition],SetRedTableValue method, IDCompositionTableTransferEffect.SetRedTableValue, IDCompositionTableTransferEffect.SetRedTableValue(UINT,IDCompositionAnimation), IDCompositionTableTransferEffect::SetRedTableValue, IDCompositionTableTransferEffect::SetRedTableValue(UINT,IDCompositionAnimation), SetRedTableValue, SetRedTableValue method [DirectComposition], SetRedTableValue method [DirectComposition],IDCompositionTableTransferEffect interface, dcomp/IDCompositionTableTransferEffect::SetRedTableValue, directcomp.idcompositiontabletransfereffect_setredtablevalue_2
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
 - IDCompositionTableTransferEffect::SetRedTableValue
 - dcomp/IDCompositionTableTransferEffect::SetRedTableValue
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
 - IDCompositionTableTransferEffect.SetRedTableValue
---

# IDCompositionTableTransferEffect::SetRedTableValue(UINT,IDCompositionAnimation)


## -description

Sets a value in the red table.

## -parameters

### -param index [in]

Type: <b>UINT</b>

The index of the value to set.

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the value changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontabletransfereffect">IDCompositionTableTransferEffect</a>
