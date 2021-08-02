---
UID: NF:dcomp.IDCompositionVisualDebug.EnableHeatMap
title: IDCompositionVisualDebug::EnableHeatMap (dcomp.h)
description: Enables a visual heatmap that represents overdraw regions.
helpviewer_keywords: ["EnableHeatMap","EnableHeatMap method [DirectComposition]","EnableHeatMap method [DirectComposition]","IDCompositionVisualDebug interface","IDCompositionVisualDebug interface [DirectComposition]","EnableHeatMap method","IDCompositionVisualDebug.EnableHeatMap","IDCompositionVisualDebug::EnableHeatMap","dcomp/IDCompositionVisualDebug::EnableHeatMap","directcomp.idcompositionvisualdebug_enableheatmap"]
old-location: directcomp\idcompositionvisualdebug_enableheatmap.htm
tech.root: directcomp
ms.assetid: 9512959B-561F-4B43-9C7E-37174CC642EB
ms.date: 12/05/2018
ms.keywords: EnableHeatMap, EnableHeatMap method [DirectComposition], EnableHeatMap method [DirectComposition],IDCompositionVisualDebug interface, IDCompositionVisualDebug interface [DirectComposition],EnableHeatMap method, IDCompositionVisualDebug.EnableHeatMap, IDCompositionVisualDebug::EnableHeatMap, dcomp/IDCompositionVisualDebug::EnableHeatMap, directcomp.idcompositionvisualdebug_enableheatmap
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
 - IDCompositionVisualDebug::EnableHeatMap
 - dcomp/IDCompositionVisualDebug::EnableHeatMap
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
 - IDCompositionVisualDebug.EnableHeatMap
---

# IDCompositionVisualDebug::EnableHeatMap


## -description

Enables a visual heatmap that represents overdraw regions.

## -parameters

### -param color [in]

## -returns

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

Heatmaps can be enabled by calling <b>EnableHeatMap</b>. The heatmaps are drawn on the source of the VisualDebug visual and child visuals. The heatmaps are represented in a specified color for all visual content. The heatmap color must have a transparency in order to see the overlaying overdraw regions. The colored surfaces are blended together to visually show all overdraw regions in a single view.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevicedebug">IDCompositionDeviceDebug</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisualdebug">IDCompositionVisualDebug</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisualdebug-disableheatmap">IDCompositionVisualDebug::DisableHeatMap</a>