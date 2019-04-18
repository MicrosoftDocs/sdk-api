---
UID: NF:tuner.IESEventServiceConfiguration.RemoveGraph
title: IESEventServiceConfiguration::RemoveGraph (tuner.h)
author: windows-sdk-content
description: Removes an event service that implements the IESEventService interface from a filter graph. This method prevents the processing of events from Protected Broadcast Driver Architecture (PBDA) devices in the graph.
old-location: mstv\ieseventserviceconfiguration_removegraph.htm
tech.root: mstv
ms.assetid: ba3d9748-5d3b-49ec-ac69-287a253caa12
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IESEventServiceConfiguration interface [Microsoft TV Technologies],RemoveGraph method, IESEventServiceConfiguration.RemoveGraph, IESEventServiceConfiguration::RemoveGraph, RemoveGraph, RemoveGraph method [Microsoft TV Technologies], RemoveGraph method [Microsoft TV Technologies],IESEventServiceConfiguration interface, mstv.ieseventserviceconfiguration_removegraph, tuner/IESEventServiceConfiguration::RemoveGraph
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESEventServiceConfiguration.RemoveGraph
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESEventServiceConfiguration::RemoveGraph


## -description


Removes an event service that implements the <a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a> interface from a filter  graph. This method prevents the processing of events from Protected Broadcast Driver Architecture (PBDA) devices in the graph. 


## -parameters




### -param pGraph [in]

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd389989(v=VS.85).aspx">IFilterGraph</a> interface for the event service that is removed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a>



<a href="https://msdn.microsoft.com/0b901732-42e1-4f50-904c-75d8202bb5b7">IESEventServiceConfiguration</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd389989(v=VS.85).aspx">IFilterGraph</a>
 

 

