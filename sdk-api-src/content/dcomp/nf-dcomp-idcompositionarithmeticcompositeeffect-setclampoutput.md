---
UID: NF:dcomp.IDCompositionArithmeticCompositeEffect.SetClampOutput
title: IDCompositionArithmeticCompositeEffect::SetClampOutput
author: windows-sdk-content
description: Specifies whether to clamp color values before the effect passes the values to the next effect in the graph.
old-location: directcomp\idcompositionarithmeticcompositeeffect_setclampoutput.htm
tech.root: directcomp
ms.assetid: 6558E6E7-FEF3-43F0-8508-197BA1DE3D10
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDCompositionArithmeticCompositeEffect interface [DirectComposition],SetClampOutput method, IDCompositionArithmeticCompositeEffect.SetClampOutput, IDCompositionArithmeticCompositeEffect::SetClampOutput, SetClampOutput, SetClampOutput method [DirectComposition], SetClampOutput method [DirectComposition],IDCompositionArithmeticCompositeEffect interface, dcomp/IDCompositionArithmeticCompositeEffect::SetClampOutput, directcomp.idcompositionarithmeticcompositeeffect_setclampoutput
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
 - IDCompositionArithmeticCompositeEffect.SetClampOutput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionArithmeticCompositeEffect::SetClampOutput


## -description


Specifies whether to clamp color values before the effect passes the values to the next effect in the graph.


## -parameters




### -param clampoutput [in]

Type: <b>BOOL</b>

A boolean value indicating whether to clamp the color values.  A value of TRUE causes color values to be clamped between 0 and 1.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/06430DD6-B6BF-4F55-A99C-13860B800444">IDCompositionArithmeticCompositeEffect</a>
 

 

