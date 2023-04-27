---
UID: NF:dcomp.IDCompositionTableTransferEffect.SetBlueTableValue(UINT,IDCompositionAnimation)
title: IDCompositionTableTransferEffect::SetBlueTableValue(UINT,IDCompositionAnimation) (dcomp.h)
description: Sets a value in the blue table. (overload 1/2)
helpviewer_keywords: ["IDCompositionTableTransferEffect interface [DirectComposition]","SetBlueTableValue method","IDCompositionTableTransferEffect.SetBlueTableValue","IDCompositionTableTransferEffect.SetBlueTableValue(UINT","IDCompositionAnimation)","IDCompositionTableTransferEffect::SetBlueTableValue","IDCompositionTableTransferEffect::SetBlueTableValue(UINT","IDCompositionAnimation)","SetBlueTableValue","SetBlueTableValue method [DirectComposition]","SetBlueTableValue method [DirectComposition]","IDCompositionTableTransferEffect interface","dcomp/IDCompositionTableTransferEffect::SetBlueTableValue","directcomp.idcompositiontabletransfereffect_setbluetablevalue_2"]
old-location: directcomp\idcompositiontabletransfereffect_setbluetablevalue_2.htm
tech.root: directcomp
ms.assetid: 82CF79D8-1CA6-4A02-B806-4A2672B4BBF3
ms.date: 12/05/2018
ms.keywords: IDCompositionTableTransferEffect interface [DirectComposition],SetBlueTableValue method, IDCompositionTableTransferEffect.SetBlueTableValue, IDCompositionTableTransferEffect.SetBlueTableValue(UINT,IDCompositionAnimation), IDCompositionTableTransferEffect::SetBlueTableValue, IDCompositionTableTransferEffect::SetBlueTableValue(UINT,IDCompositionAnimation), SetBlueTableValue, SetBlueTableValue method [DirectComposition], SetBlueTableValue method [DirectComposition],IDCompositionTableTransferEffect interface, dcomp/IDCompositionTableTransferEffect::SetBlueTableValue, directcomp.idcompositiontabletransfereffect_setbluetablevalue_2
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
 - IDCompositionTableTransferEffect::SetBlueTableValue
 - dcomp/IDCompositionTableTransferEffect::SetBlueTableValue
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
 - IDCompositionTableTransferEffect.SetBlueTableValue
---

# IDCompositionTableTransferEffect::SetBlueTableValue(UINT,IDCompositionAnimation)


## -description

Sets a value in the blue table.

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
