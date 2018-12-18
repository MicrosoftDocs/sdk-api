---
UID: NF:dcomp.IDCompositionTableTransferEffect.SetRedTableValue(UINT,IDCompositionAnimation)
title: IDCompositionTableTransferEffect::SetRedTableValue(UINT,IDCompositionAnimation)
author: windows-sdk-content
description: Sets a value in the red table.
old-location: directcomp\idcompositiontabletransfereffect_setredtablevalue_2.htm
tech.root: directcomp
ms.assetid: 983E302A-F13C-48A7-9C9F-9569EB4585D3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionTableTransferEffect interface [DirectComposition],SetRedTableValue method, IDCompositionTableTransferEffect.SetRedTableValue, IDCompositionTableTransferEffect.SetRedTableValue(UINT,IDCompositionAnimation), IDCompositionTableTransferEffect::SetRedTableValue, IDCompositionTableTransferEffect::SetRedTableValue(UINT,IDCompositionAnimation), SetRedTableValue, SetRedTableValue method [DirectComposition], SetRedTableValue method [DirectComposition],IDCompositionTableTransferEffect interface, dcomp/IDCompositionTableTransferEffect::SetRedTableValue, directcomp.idcompositiontabletransfereffect_setredtablevalue_2
ms.topic: method
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
 - IDCompositionTableTransferEffect.SetRedTableValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionTableTransferEffect::SetRedTableValue(UINT,IDCompositionAnimation)


## -description


Sets a value in the red table.


## -parameters




### -param index [in]

Type: <b>UINT</b>

The index of the value to set.


### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation that represents how the value changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/147E15B8-C529-4BC6-85AA-FB069B892C6C">IDCompositionTableTransferEffect</a>
 

 

