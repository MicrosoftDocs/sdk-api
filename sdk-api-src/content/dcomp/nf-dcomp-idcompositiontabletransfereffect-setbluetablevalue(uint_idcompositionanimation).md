---
UID: NF:dcomp.IDCompositionTableTransferEffect.SetBlueTableValue(UINT,IDCompositionAnimation)
title: IDCompositionTableTransferEffect::SetBlueTableValue(UINT,IDCompositionAnimation)
author: windows-sdk-content
description: Sets a value in the blue table.
old-location: directcomp\idcompositiontabletransfereffect_setbluetablevalue_2.htm
tech.root: directcomp
ms.assetid: 82CF79D8-1CA6-4A02-B806-4A2672B4BBF3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionTableTransferEffect interface [DirectComposition],SetBlueTableValue method, IDCompositionTableTransferEffect.SetBlueTableValue, IDCompositionTableTransferEffect.SetBlueTableValue(UINT,IDCompositionAnimation), IDCompositionTableTransferEffect::SetBlueTableValue, IDCompositionTableTransferEffect::SetBlueTableValue(UINT,IDCompositionAnimation), SetBlueTableValue, SetBlueTableValue method [DirectComposition], SetBlueTableValue method [DirectComposition],IDCompositionTableTransferEffect interface, dcomp/IDCompositionTableTransferEffect::SetBlueTableValue, directcomp.idcompositiontabletransfereffect_setbluetablevalue_2
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
 - IDCompositionTableTransferEffect.SetBlueTableValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionTableTransferEffect::SetBlueTableValue(UINT,IDCompositionAnimation)


## -description


Sets a value in the blue table.


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
 

 

