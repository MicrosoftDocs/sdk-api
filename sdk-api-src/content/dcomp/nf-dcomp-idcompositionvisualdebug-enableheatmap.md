---
UID: NF:dcomp.IDCompositionVisualDebug.EnableHeatMap
title: IDCompositionVisualDebug::EnableHeatMap
author: windows-sdk-content
description: Enables a visual heatmap that represents overdraw regions.
old-location: directcomp\idcompositionvisualdebug_enableheatmap.htm
tech.root: directcomp
ms.assetid: 9512959B-561F-4B43-9C7E-37174CC642EB
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EnableHeatMap, EnableHeatMap method [DirectComposition], EnableHeatMap method [DirectComposition],IDCompositionVisualDebug interface, IDCompositionVisualDebug interface [DirectComposition],EnableHeatMap method, IDCompositionVisualDebug.EnableHeatMap, IDCompositionVisualDebug::EnableHeatMap, dcomp/IDCompositionVisualDebug::EnableHeatMap, directcomp.idcompositionvisualdebug_enableheatmap
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
 - IDCompositionVisualDebug.EnableHeatMap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dcomp.h
: 
- IDCompositionVisualDebug.EnableHeatMap
: 
---

# IDCompositionVisualDebug::EnableHeatMap


## -description


Enables a visual heatmap that represents overdraw regions.


## -parameters




### -param color [in]


## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



Heatmaps can be enabled by calling <b>EnableHeatMap</b>. The heatmaps are drawn on the source of the VisualDebug visual and child visuals. The heatmaps are represented in a specified color for all visual content. The heatmap color must have an transparency in order to see the overlaying overdraw regions. The colored surfaces are blended together to visually show all overdraw regions in a single view. 




## -see-also




<a href="https://msdn.microsoft.com/B8D17570-9729-45DB-99E1-A2EBBDAA5996">IDCompositionDeviceDebug</a>



<a href="https://msdn.microsoft.com/0AF98EEB-3EA7-44E3-8F2F-182D9F6BCCA4">IDCompositionVisualDebug</a>



<a href="https://msdn.microsoft.com/C186E930-4523-4DF7-8E74-B69AF91622F4">IDCompositionVisualDebug::DisableHeatMap</a>
 

 

