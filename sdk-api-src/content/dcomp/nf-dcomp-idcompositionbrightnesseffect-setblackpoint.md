---
UID: NF:dcomp.IDCompositionBrightnessEffect.SetBlackPoint
title: IDCompositionBrightnessEffect::SetBlackPoint
author: windows-sdk-content
description: Specifies the lower portion of the brightness transfer curve for the brightness effect.
old-location: directcomp\idcompositionbrightnesseffect_setblackpoint.htm
tech.root: directcomp
ms.assetid: C63F0F4C-6C25-495A-8AD8-F1A453E0B4BA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionBrightnessEffect interface [DirectComposition],SetBlackPoint method, IDCompositionBrightnessEffect.SetBlackPoint, IDCompositionBrightnessEffect::SetBlackPoint, SetBlackPoint, SetBlackPoint method [DirectComposition], SetBlackPoint method [DirectComposition],IDCompositionBrightnessEffect interface, dcomp/IDCompositionBrightnessEffect::SetBlackPoint, directcomp.idcompositionbrightnesseffect_setblackpoint
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
 - IDCompositionBrightnessEffect.SetBlackPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionBrightnessEffect::SetBlackPoint


## -description


Specifies the lower portion of the brightness transfer curve for the brightness effect.


## -parameters




### -param blackPoint [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a></b>

The lower portion of the brightness transfer curve. The black point adjusts the appearance of the darker portions of the image. The vector is for both the x value and the y value, in that order. Each of the values must be between 0 and 1, inclusive.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn919711(v=VS.85).aspx">IDCompositionBrightnessEffect</a>
 

 

