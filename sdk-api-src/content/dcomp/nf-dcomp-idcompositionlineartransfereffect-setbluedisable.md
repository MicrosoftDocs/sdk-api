---
UID: NF:dcomp.IDCompositionLinearTransferEffect.SetBlueDisable
title: IDCompositionLinearTransferEffect::SetBlueDisable
author: windows-sdk-content
description: Specifies whether to apply the transfer function to the blue channel.
old-location: directcomp\idcompositionlineartransfereffect_setbluedisable.htm
tech.root: directcomp
ms.assetid: DE87E53B-4469-4B30-8397-6A0712DE8A6C
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDCompositionLinearTransferEffect interface [DirectComposition],SetBlueDisable method, IDCompositionLinearTransferEffect.SetBlueDisable, IDCompositionLinearTransferEffect::SetBlueDisable, SetBlueDisable, SetBlueDisable method [DirectComposition], SetBlueDisable method [DirectComposition],IDCompositionLinearTransferEffect interface, dcomp/IDCompositionLinearTransferEffect::SetBlueDisable, directcomp.idcompositionlineartransfereffect_setbluedisable
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
 - IDCompositionLinearTransferEffect.SetBlueDisable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionLinearTransferEffect::SetBlueDisable


## -description


Specifies whether to apply the transfer function to the blue channel.


## -parameters




### -param blueDisable [in]

Type: <b>BOOL</b>

A boolean value that specifies whether to apply the transfer function to the blue channel.
            If you set this to TRUE the effect does not apply the transfer function to the blue channel. If you set this to FALSE it applies the BlueLinearTransfer function to the blue channel.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/516CD029-DBB1-4AD7-92BB-8B6EF6C733FA">IDCompositionLinearTransferEffect</a>
 

 

