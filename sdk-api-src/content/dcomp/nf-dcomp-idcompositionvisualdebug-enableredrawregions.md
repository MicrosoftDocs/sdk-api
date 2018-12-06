---
UID: NF:dcomp.IDCompositionVisualDebug.EnableRedrawRegions
title: IDCompositionVisualDebug::EnableRedrawRegions
author: windows-sdk-content
description: Enables highlighting visuals when content is being redrawn.
old-location: directcomp\idcompositionvisualdebug_enableredrawregions.htm
tech.root: directcomp
ms.assetid: 71591ABF-7B7F-4A8D-9FE2-EC5412ACB3EE
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnableRedrawRegions, EnableRedrawRegions method [DirectComposition], EnableRedrawRegions method [DirectComposition],IDCompositionVisualDebug interface, IDCompositionVisualDebug interface [DirectComposition],EnableRedrawRegions method, IDCompositionVisualDebug.EnableRedrawRegions, IDCompositionVisualDebug::EnableRedrawRegions, dcomp/IDCompositionVisualDebug::EnableRedrawRegions, directcomp.idcompositionvisualdebug_enableredrawregions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDCompositionVisualDebug.EnableRedrawRegions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVisualDebug::EnableRedrawRegions


## -description


Enables highlighting visuals when content is being redrawn.


## -parameters






## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



Highlighting redraw regions can be enabled by calling <b>EnableRedrawRegions</b>.  With this function, redrawn client areas are visually highlighted every frame the visual is updated. Redraw regions are drawn on the source of the VisualDebug and child visuals. Redraw is triggered when properties of a visual are updated. The updated visusal does not neccessarly need to visually change to trigger a redraw. The highlighting will cycle through Blue, Yellow, Pink and Green to provide an order of which content is being updated. The redraw regions are only visible while the window of the VisualDebug is being updated. 




## -see-also




<a href="https://msdn.microsoft.com/B8D17570-9729-45DB-99E1-A2EBBDAA5996">IDCompositionDeviceDebug</a>



<a href="https://msdn.microsoft.com/0AF98EEB-3EA7-44E3-8F2F-182D9F6BCCA4">IDCompositionVisualDebug</a>



<a href="https://msdn.microsoft.com/5F1712D4-B3F4-475E-9AB0-868B1DCB8F42">IDCompositionVisualDebug::DisableRedrawRegions</a>
 

 

