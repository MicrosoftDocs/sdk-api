---
UID: NF:dcomp.IDCompositionTableTransferEffect.SetGreenTableValue(UINT,IDCompositionAnimation)
title: IDCompositionTableTransferEffect::SetGreenTableValue(UINT,IDCompositionAnimation)
author: windows-sdk-content
description: Sets a value in the green table.
old-location: directcomp\idcompositiontabletransfereffect_setgreentablevalue_2.htm
tech.root: directcomp
ms.assetid: 841850FD-A94A-45F8-8D24-B91D4522EA2E
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDCompositionTableTransferEffect interface [DirectComposition],SetGreenTableValue method, IDCompositionTableTransferEffect.SetGreenTableValue, IDCompositionTableTransferEffect.SetGreenTableValue(UINT,IDCompositionAnimation), IDCompositionTableTransferEffect::SetGreenTableValue, IDCompositionTableTransferEffect::SetGreenTableValue(UINT,IDCompositionAnimation), SetGreenTableValue, SetGreenTableValue method [DirectComposition], SetGreenTableValue method [DirectComposition],IDCompositionTableTransferEffect interface, dcomp/IDCompositionTableTransferEffect::SetGreenTableValue, directcomp.idcompositiontabletransfereffect_setgreentablevalue_2
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDCompositionTableTransferEffect.SetGreenTableValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionTableTransferEffect::SetGreenTableValue(UINT,IDCompositionAnimation)


## -description


Sets a value in the green table.


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
 

 

