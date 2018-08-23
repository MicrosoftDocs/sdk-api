---
UID: NF:dcomp.IDCompositionTableTransferEffect.SetClampOutput
title: IDCompositionTableTransferEffect::SetClampOutput
author: windows-sdk-content
description: Specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.
old-location: directcomp\idcompositiontabletransfereffect_setclampoutput.htm
old-project: directcomp
ms.assetid: 6F1A7757-92DA-4BDC-9894-7A8906461FD5
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionTableTransferEffect interface [DirectComposition],SetClampOutput method, IDCompositionTableTransferEffect.SetClampOutput, IDCompositionTableTransferEffect::SetClampOutput, SetClampOutput, SetClampOutput method [DirectComposition], SetClampOutput method [DirectComposition],IDCompositionTableTransferEffect interface, dcomp/IDCompositionTableTransferEffect::SetClampOutput, directcomp.idcompositiontabletransfereffect_setclampoutput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D_VECTOR_4F
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionTableTransferEffect.SetClampOutput
product: Windows
targetos: Windows
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# IDCompositionTableTransferEffect::SetClampOutput


## -description


Specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.


## -parameters




### -param clampOutput [in]

Type: <b>BOOL</b>

A boolean value that specifies whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.
            If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values,
            but other effects and the output surface may clamp the values if they are not of high enough precision.
            The effect clamps the values before it premultiplies the alpha.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/147E15B8-C529-4BC6-85AA-FB069B892C6C">IDCompositionTableTransferEffect</a>
 

 

