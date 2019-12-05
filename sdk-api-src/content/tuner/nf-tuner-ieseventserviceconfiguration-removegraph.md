---
UID: NF:tuner.IESEventServiceConfiguration.RemoveGraph
title: IESEventServiceConfiguration::RemoveGraph (tuner.h)
description: Removes an event service that implements the IESEventService interface from a filter graph. This method prevents the processing of events from Protected Broadcast Driver Architecture (PBDA) devices in the graph.
old-location: mstv\ieseventserviceconfiguration_removegraph.htm
tech.root: mstv
ms.assetid: ba3d9748-5d3b-49ec-ac69-287a253caa12
ms.date: 12/05/2018
ms.keywords: IESEventServiceConfiguration interface [Microsoft TV Technologies],RemoveGraph method, IESEventServiceConfiguration.RemoveGraph, IESEventServiceConfiguration::RemoveGraph, RemoveGraph, RemoveGraph method [Microsoft TV Technologies], RemoveGraph method [Microsoft TV Technologies],IESEventServiceConfiguration interface, mstv.ieseventserviceconfiguration_removegraph, tuner/IESEventServiceConfiguration::RemoveGraph
ms.topic: method
f1_keywords:
- tuner/IESEventServiceConfiguration.RemoveGraph
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESEventServiceConfiguration::RemoveGraph


## -description


Removes an event service that implements the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a> interface from a filter  graph. This method prevents the processing of events from Protected Broadcast Driver Architecture (PBDA) devices in the graph. 


## -parameters




### -param pGraph [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a> interface for the event service that is removed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventserviceconfiguration">IESEventServiceConfiguration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a>
 

 

