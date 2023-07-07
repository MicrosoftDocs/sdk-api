---
UID: NF:tuner.IESEventServiceConfiguration.SetOwner
title: IESEventServiceConfiguration::SetOwner (tuner.h)
description: Adds an owner to an event service, where event service refers to a generic Windows event service that implements the IESEventService interface.
helpviewer_keywords: ["IESEventServiceConfiguration interface [Microsoft TV Technologies]","SetOwner method","IESEventServiceConfiguration.SetOwner","IESEventServiceConfiguration::SetOwner","SetOwner","SetOwner method [Microsoft TV Technologies]","SetOwner method [Microsoft TV Technologies]","IESEventServiceConfiguration interface","mstv.ieseventserviceconfiguration_setowner","tuner/IESEventServiceConfiguration::SetOwner"]
old-location: mstv\ieseventserviceconfiguration_setowner.htm
tech.root: mstv
ms.assetid: 7d8e1be1-b363-41ac-b60b-98415f0f44b6
ms.date: 12/05/2018
ms.keywords: IESEventServiceConfiguration interface [Microsoft TV Technologies],SetOwner method, IESEventServiceConfiguration.SetOwner, IESEventServiceConfiguration::SetOwner, SetOwner, SetOwner method [Microsoft TV Technologies], SetOwner method [Microsoft TV Technologies],IESEventServiceConfiguration interface, mstv.ieseventserviceconfiguration_setowner, tuner/IESEventServiceConfiguration::SetOwner
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
 - IESEventServiceConfiguration::SetOwner
 - tuner/IESEventServiceConfiguration::SetOwner
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
 - IESEventServiceConfiguration.SetOwner
---

# IESEventServiceConfiguration::SetOwner


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Adds an owner to an event service, where <i>event service</i> refers to a generic Windows event service that implements the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a> interface. The owner is the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevents">IESEvents</a> object that the parent event service uses to pass advise events to its child event service for handling.

## -parameters

### -param pESEvents [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevents">IESEvents</a> interface that the  parent event service uses to advise its child.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventserviceconfiguration">IESEventServiceConfiguration</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevents">IESEvents</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventserviceconfiguration-setparent">SetParent</a>