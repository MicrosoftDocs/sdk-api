---
UID: NF:tuner.IESEventServiceConfiguration.RemoveGraph
title: IESEventServiceConfiguration::RemoveGraph (tuner.h)
description: Removes an event service that implements the IESEventService interface from a filter graph. This method prevents the processing of events from Protected Broadcast Driver Architecture (PBDA) devices in the graph.
helpviewer_keywords: ["IESEventServiceConfiguration interface [Microsoft TV Technologies]","RemoveGraph method","IESEventServiceConfiguration.RemoveGraph","IESEventServiceConfiguration::RemoveGraph","RemoveGraph","RemoveGraph method [Microsoft TV Technologies]","RemoveGraph method [Microsoft TV Technologies]","IESEventServiceConfiguration interface","mstv.ieseventserviceconfiguration_removegraph","tuner/IESEventServiceConfiguration::RemoveGraph"]
old-location: mstv\ieseventserviceconfiguration_removegraph.htm
tech.root: mstv
ms.assetid: ba3d9748-5d3b-49ec-ac69-287a253caa12
ms.date: 12/05/2018
ms.keywords: IESEventServiceConfiguration interface [Microsoft TV Technologies],RemoveGraph method, IESEventServiceConfiguration.RemoveGraph, IESEventServiceConfiguration::RemoveGraph, RemoveGraph, RemoveGraph method [Microsoft TV Technologies], RemoveGraph method [Microsoft TV Technologies],IESEventServiceConfiguration interface, mstv.ieseventserviceconfiguration_removegraph, tuner/IESEventServiceConfiguration::RemoveGraph
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IESEventServiceConfiguration::RemoveGraph
 - tuner/IESEventServiceConfiguration::RemoveGraph
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESEventServiceConfiguration.RemoveGraph
---

# IESEventServiceConfiguration::RemoveGraph


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Removes an event service that implements the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a> interface from a filter  graph. This method prevents the processing of events from Protected Broadcast Driver Architecture (PBDA) devices in the graph.

## -parameters

### -param pGraph [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a> interface for the event service that is removed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventserviceconfiguration">IESEventServiceConfiguration</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a>