---
UID: NF:tuner.IESEventServiceConfiguration.RemoveGraph
title: IESEventServiceConfiguration::RemoveGraph
author: windows-sdk-content
description: Removes an event service that implements the IESEventService interface from a filter graph. This method prevents the processing of events from Protected Broadcast Driver Architecture (PBDA) devices in the graph.
old-location: mstv\ieseventserviceconfiguration_removegraph.htm
old-project: mstv
ms.assetid: ba3d9748-5d3b-49ec-ac69-287a253caa12
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IESEventServiceConfiguration interface [Microsoft TV Technologies],RemoveGraph method, IESEventServiceConfiguration.RemoveGraph, IESEventServiceConfiguration::RemoveGraph, RemoveGraph, RemoveGraph method [Microsoft TV Technologies], RemoveGraph method [Microsoft TV Technologies],IESEventServiceConfiguration interface, mstv.ieseventserviceconfiguration_removegraph, tuner/IESEventServiceConfiguration::RemoveGraph
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IESEventServiceConfiguration.RemoveGraph
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESEventServiceConfiguration::RemoveGraph


## -description



      Removes an event service that implements the <a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a> interface from a filter  graph. This method prevents the processing of events from Protected Broadcast Driver Architecture (PBDA) devices in the graph. 


## -parameters




### -param pGraph [in]

Pointer to the <a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph</a> interface for the event service that is removed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a>



<a href="https://msdn.microsoft.com/0b901732-42e1-4f50-904c-75d8202bb5b7">IESEventServiceConfiguration</a>



<a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph</a>
 

 

