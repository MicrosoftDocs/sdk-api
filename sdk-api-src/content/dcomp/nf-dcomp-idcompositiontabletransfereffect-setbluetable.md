---
UID: NF:dcomp.IDCompositionTableTransferEffect.SetBlueTable
title: IDCompositionTableTransferEffect::SetBlueTable (dcomp.h)
description: Sets the list of values used to define the transfer function for the blue channel.
helpviewer_keywords: ["IDCompositionTableTransferEffect interface [DirectComposition]","SetBlueTable method","IDCompositionTableTransferEffect.SetBlueTable","IDCompositionTableTransferEffect::SetBlueTable","SetBlueTable","SetBlueTable method [DirectComposition]","SetBlueTable method [DirectComposition]","IDCompositionTableTransferEffect interface","dcomp/IDCompositionTableTransferEffect::SetBlueTable","directcomp.idcompositiontabletransfereffect_setbluetable"]
old-location: directcomp\idcompositiontabletransfereffect_setbluetable.htm
tech.root: directcomp
ms.assetid: D6E5D8CB-8E69-4E33-AC2E-4995F9D4283A
ms.date: 12/05/2018
ms.keywords: IDCompositionTableTransferEffect interface [DirectComposition],SetBlueTable method, IDCompositionTableTransferEffect.SetBlueTable, IDCompositionTableTransferEffect::SetBlueTable, SetBlueTable, SetBlueTable method [DirectComposition], SetBlueTable method [DirectComposition],IDCompositionTableTransferEffect interface, dcomp/IDCompositionTableTransferEffect::SetBlueTable, directcomp.idcompositiontabletransfereffect_setbluetable
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
 - IDCompositionTableTransferEffect::SetBlueTable
 - dcomp/IDCompositionTableTransferEffect::SetBlueTable
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
 - IDCompositionTableTransferEffect.SetBlueTable
---

# IDCompositionTableTransferEffect::SetBlueTable


## -description

Sets the list of values used to define the transfer function for the blue channel.

## -parameters

### -param tableValues [in]

Type: <b>const float*</b>

The list of values used to define the transfer function for the blue channel.

### -param count [in]

Type: <b>UINT</b>

The number of values in the tableValues parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontabletransfereffect">IDCompositionTableTransferEffect</a>