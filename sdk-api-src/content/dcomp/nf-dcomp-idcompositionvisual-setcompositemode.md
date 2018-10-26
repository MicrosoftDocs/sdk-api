---
UID: NF:dcomp.IDCompositionVisual.SetCompositeMode
title: IDCompositionVisual::SetCompositeMode
author: windows-sdk-content
description: Sets the blending mode for this visual.
old-location: directcomp\idcompositionvisual_setcompositemode.htm
tech.root: directcomp
ms.assetid: 2F8C7930-6BBC-4CA9-86C0-168BF0F9C0BD
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetCompositeMode method, IDCompositionVisual.SetCompositeMode, IDCompositionVisual::SetCompositeMode, SetCompositeMode, SetCompositeMode method [DirectComposition], SetCompositeMode method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetCompositeMode, directcomp.idcompositionvisual_setcompositemode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IDCompositionVisual.SetCompositeMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVisual::SetCompositeMode


## -description


Sets the blending mode for this visual.


## -parameters




### -param compositeMode [in]

Type: <b><a href="https://msdn.microsoft.com/D89379F5-57F8-4838-8E8F-FF261D69DE59">DCOMPOSITION_COMPOSITE_MODE</a></b>

The blending mode to use when composing the visual to the screen.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



The composite mode determines how visual's bitmap is blended with the screen. By default, the visual is blended with "source over" semantics; that is, the colors are blended with per-pixel transparency.




## -see-also




<a href="https://msdn.microsoft.com/B8C5A4D8-F161-4383-B117-B89E85C65B19">IDCompositionEffectGroup</a>



<a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>
 

 

