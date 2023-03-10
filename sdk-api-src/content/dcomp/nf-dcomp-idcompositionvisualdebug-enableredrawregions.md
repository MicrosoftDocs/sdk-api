---
UID: NF:dcomp.IDCompositionVisualDebug.EnableRedrawRegions
title: IDCompositionVisualDebug::EnableRedrawRegions (dcomp.h)
description: Enables highlighting visuals when content is being redrawn.
helpviewer_keywords: ["EnableRedrawRegions","EnableRedrawRegions method [DirectComposition]","EnableRedrawRegions method [DirectComposition]","IDCompositionVisualDebug interface","IDCompositionVisualDebug interface [DirectComposition]","EnableRedrawRegions method","IDCompositionVisualDebug.EnableRedrawRegions","IDCompositionVisualDebug::EnableRedrawRegions","dcomp/IDCompositionVisualDebug::EnableRedrawRegions","directcomp.idcompositionvisualdebug_enableredrawregions"]
old-location: directcomp\idcompositionvisualdebug_enableredrawregions.htm
tech.root: directcomp
ms.assetid: 71591ABF-7B7F-4A8D-9FE2-EC5412ACB3EE
ms.date: 12/05/2018
ms.keywords: EnableRedrawRegions, EnableRedrawRegions method [DirectComposition], EnableRedrawRegions method [DirectComposition],IDCompositionVisualDebug interface, IDCompositionVisualDebug interface [DirectComposition],EnableRedrawRegions method, IDCompositionVisualDebug.EnableRedrawRegions, IDCompositionVisualDebug::EnableRedrawRegions, dcomp/IDCompositionVisualDebug::EnableRedrawRegions, directcomp.idcompositionvisualdebug_enableredrawregions
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionVisualDebug::EnableRedrawRegions
 - dcomp/IDCompositionVisualDebug::EnableRedrawRegions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionVisualDebug.EnableRedrawRegions
---

# IDCompositionVisualDebug::EnableRedrawRegions


## -description

Enables highlighting visuals when content is being redrawn.



## -returns

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

Highlighting redraw regions can be enabled by calling <b>EnableRedrawRegions</b>.  With this function, redrawn client areas are visually highlighted every frame the visual is updated. Redraw regions are drawn on the source of the VisualDebug and child visuals. Redraw is triggered when properties of a visual are updated. The updated visual does not necessarily need to visually change to trigger a redraw. The highlighting will cycle through Blue, Yellow, Pink and Green to provide an order of which content is being updated. The redraw regions are only visible while the window of the VisualDebug is being updated.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevicedebug">IDCompositionDeviceDebug</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisualdebug">IDCompositionVisualDebug</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisualdebug-disableredrawregions">IDCompositionVisualDebug::DisableRedrawRegions</a>
