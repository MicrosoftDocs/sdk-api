---
UID: NF:dcomp.IDCompositionVisualDebug.EnableHeatMap
title: IDCompositionVisualDebug::EnableHeatMap (dcomp.h)
author: windows-sdk-content
description: Enables a visual heatmap that represents overdraw regions.
old-location: directcomp\idcompositionvisualdebug_enableheatmap.htm
tech.root: directcomp
ms.assetid: 9512959B-561F-4B43-9C7E-37174CC642EB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnableHeatMap, EnableHeatMap method [DirectComposition], EnableHeatMap method [DirectComposition],IDCompositionVisualDebug interface, IDCompositionVisualDebug interface [DirectComposition],EnableHeatMap method, IDCompositionVisualDebug.EnableHeatMap, IDCompositionVisualDebug::EnableHeatMap, dcomp/IDCompositionVisualDebug::EnableHeatMap, directcomp.idcompositionvisualdebug_enableheatmap
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionVisualDebug.EnableHeatMap"
dev_langs:
 - c++
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
 - IDCompositionVisualDebug.EnableHeatMap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionVisualDebug::EnableHeatMap


## -description


Enables a visual heatmap that represents overdraw regions.


## -parameters




### -param color [in]


## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



Heatmaps can be enabled by calling <b>EnableHeatMap</b>. The heatmaps are drawn on the source of the VisualDebug visual and child visuals. The heatmaps are represented in a specified color for all visual content. The heatmap color must have an transparency in order to see the overlaying overdraw regions. The colored surfaces are blended together to visually show all overdraw regions in a single view. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevicedebug">IDCompositionDeviceDebug</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisualdebug">IDCompositionVisualDebug</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisualdebug-disableheatmap">IDCompositionVisualDebug::DisableHeatMap</a>
 

 

