---
UID: NF:dcomp.IDCompositionTableTransferEffect.SetRedTable
title: IDCompositionTableTransferEffect::SetRedTable (dcomp.h)
author: windows-sdk-content
description: Sets the list of values used to define the transfer function for the red channel.
old-location: directcomp\idcompositiontabletransfereffect_setredtable.htm
tech.root: directcomp
ms.assetid: 4113919E-84B9-402A-A2A1-64EB74D2CC59
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionTableTransferEffect interface [DirectComposition],SetRedTable method, IDCompositionTableTransferEffect.SetRedTable, IDCompositionTableTransferEffect::SetRedTable, SetRedTable, SetRedTable method [DirectComposition], SetRedTable method [DirectComposition],IDCompositionTableTransferEffect interface, dcomp/IDCompositionTableTransferEffect::SetRedTable, directcomp.idcompositiontabletransfereffect_setredtable
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionTableTransferEffect.SetRedTable"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionTableTransferEffect.SetRedTable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionTableTransferEffect::SetRedTable


## -description


Sets the list of values used to define the transfer function for the red channel.


## -parameters




### -param tableValues [in]

Type: <b>const float*</b>

The list of values used to define the transfer function for the red channel.


### -param count [in]

Type: <b>UINT</b>

The number of values in the tableValues parameter.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontabletransfereffect">IDCompositionTableTransferEffect</a>
 

 

