---
UID: NF:dcomp.IDCompositionTableTransferEffect.SetBlueDisable
title: IDCompositionTableTransferEffect::SetBlueDisable (dcomp.h)
author: windows-sdk-content
description: Specifies whether to apply the transfer function to the blue channel.
old-location: directcomp\idcompositiontabletransfereffect_setbluedisable.htm
tech.root: directcomp
ms.assetid: 278FE30E-86F2-4E34-AED5-78C699FC2319
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionTableTransferEffect interface [DirectComposition],SetBlueDisable method, IDCompositionTableTransferEffect.SetBlueDisable, IDCompositionTableTransferEffect::SetBlueDisable, SetBlueDisable, SetBlueDisable method [DirectComposition], SetBlueDisable method [DirectComposition],IDCompositionTableTransferEffect interface, dcomp/IDCompositionTableTransferEffect::SetBlueDisable, directcomp.idcompositiontabletransfereffect_setbluedisable
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
 - IDCompositionTableTransferEffect.SetBlueDisable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionTableTransferEffect::SetBlueDisable


## -description


Specifies whether to apply the transfer function to the blue channel.


## -parameters




### -param blueDisable [in]

Type: <b>BOOL</b>

A boolean value that specifies whether to apply the transfer function to the blue channel.
            If you set this to TRUE the effect does not apply the transfer function to the blue channel. If you set this to FALSE it applies the BlueTableTransfer function to the Blue channel.
          


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontabletransfereffect">IDCompositionTableTransferEffect</a>
 

 

