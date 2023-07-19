---
UID: NF:tuner.IESEventServiceConfiguration.SetGraph
title: IESEventServiceConfiguration::SetGraph (tuner.h)
description: Attaches an event service that implements the IESEventService interface to a filter graph. This method allows the processing of events that support the IESEvent interface from devices in the graph.
helpviewer_keywords: ["IESEventServiceConfiguration interface [Microsoft TV Technologies]","SetGraph method","IESEventServiceConfiguration.SetGraph","IESEventServiceConfiguration::SetGraph","SetGraph","SetGraph method [Microsoft TV Technologies]","SetGraph method [Microsoft TV Technologies]","IESEventServiceConfiguration interface","mstv.ieseventserviceconfiguration_setgraph","tuner/IESEventServiceConfiguration::SetGraph"]
old-location: mstv\ieseventserviceconfiguration_setgraph.htm
tech.root: mstv
ms.assetid: 0aee92b4-740a-4c5a-a64e-9de08d1c35c2
ms.date: 12/05/2018
ms.keywords: IESEventServiceConfiguration interface [Microsoft TV Technologies],SetGraph method, IESEventServiceConfiguration.SetGraph, IESEventServiceConfiguration::SetGraph, SetGraph, SetGraph method [Microsoft TV Technologies], SetGraph method [Microsoft TV Technologies],IESEventServiceConfiguration interface, mstv.ieseventserviceconfiguration_setgraph, tuner/IESEventServiceConfiguration::SetGraph
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
 - IESEventServiceConfiguration::SetGraph
 - tuner/IESEventServiceConfiguration::SetGraph
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
 - IESEventServiceConfiguration.SetGraph
---

# IESEventServiceConfiguration::SetGraph


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Attaches an event service that implements the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a>  interface to a filter  graph. This method allows the processing of events that support the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> interface from devices in the graph.

## -parameters

### -param pGraph [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a> interface that is attached to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a> event service.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventserviceconfiguration">IESEventServiceConfiguration</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a>