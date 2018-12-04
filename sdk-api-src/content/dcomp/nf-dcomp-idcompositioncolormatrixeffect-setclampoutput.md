---
UID: NF:dcomp.IDCompositionColorMatrixEffect.SetClampOutput
title: IDCompositionColorMatrixEffect::SetClampOutput
author: windows-sdk-content
description: Specifies whether the effect clamps color values to between 0 and 1 before the effects passes the values to the next effect in the chain.
old-location: directcomp\idcompositioncolormatrixeffect_setclampoutput.htm
tech.root: directcomp
ms.assetid: 2C4EF887-18CF-49A2-96F5-02B81939BBA9
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDCompositionColorMatrixEffect interface [DirectComposition],SetClampOutput method, IDCompositionColorMatrixEffect.SetClampOutput, IDCompositionColorMatrixEffect::SetClampOutput, SetClampOutput, SetClampOutput method [DirectComposition], SetClampOutput method [DirectComposition],IDCompositionColorMatrixEffect interface, dcomp/IDCompositionColorMatrixEffect::SetClampOutput, directcomp.idcompositioncolormatrixeffect_setclampoutput
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
 - IDCompositionColorMatrixEffect.SetClampOutput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionColorMatrixEffect::SetClampOutput


## -description


Specifies whether the effect clamps color values to between 0 and 1 before the effects passes the values to the next effect in the chain.


## -parameters




### -param clamp [in]

Type: <b>BOOL</b>

A boolean value indicating whether the effect clamps color values to between 0 and 1 before the effects passes the values to the next effect in the chain.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/75528E11-D041-4192-833A-31679316DF76">IDCompositionColorMatrixEffect</a>
 

 

