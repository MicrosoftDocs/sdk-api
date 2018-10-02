---
UID: NF:dcomp.IDCompositionLinearTransferEffect.SetClampOutput
title: IDCompositionLinearTransferEffect::SetClampOutput
author: windows-sdk-content
description: Specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.
old-location: directcomp\idcompositionlineartransfereffect_setclampoutput.htm
tech.root: directcomp
ms.assetid: D56B3B15-6437-46A3-B1F9-88F5BC4A9BB2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDCompositionLinearTransferEffect interface [DirectComposition],SetClampOutput method, IDCompositionLinearTransferEffect.SetClampOutput, IDCompositionLinearTransferEffect::SetClampOutput, SetClampOutput, SetClampOutput method [DirectComposition], SetClampOutput method [DirectComposition],IDCompositionLinearTransferEffect interface, dcomp/IDCompositionLinearTransferEffect::SetClampOutput, directcomp.idcompositionlineartransfereffect_setclampoutput
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
 - IDCompositionLinearTransferEffect.SetClampOutput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionLinearTransferEffect::SetClampOutput


## -description


Specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.


## -parameters




### -param clampOutput [in]

Type: <b>BOOL</b>

A boolean value that specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.
            If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values, but other effects and the output
            surface may clamp the values if they are not of high enough precision.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/516CD029-DBB1-4AD7-92BB-8B6EF6C733FA">IDCompositionLinearTransferEffect</a>
 

 

