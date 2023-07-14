---
UID: NF:tuner.IESEventServiceConfiguration.SetParent
title: IESEventServiceConfiguration::SetParent (tuner.h)
description: Sets a parent event service for an event service that implements the IESEventService interface. Once an event service has set a parent, it can receive advise events from the parent.
helpviewer_keywords: ["IESEventServiceConfiguration interface [Microsoft TV Technologies]","SetParent method","IESEventServiceConfiguration.SetParent","IESEventServiceConfiguration::SetParent","SetParent","SetParent method [Microsoft TV Technologies]","SetParent method [Microsoft TV Technologies]","IESEventServiceConfiguration interface","mstv.ieseventserviceconfiguration_setparent","tuner/IESEventServiceConfiguration::SetParent"]
old-location: mstv\ieseventserviceconfiguration_setparent.htm
tech.root: mstv
ms.assetid: cfb931e9-f20f-4812-9d6b-cf8b651b7e7a
ms.date: 12/05/2018
ms.keywords: IESEventServiceConfiguration interface [Microsoft TV Technologies],SetParent method, IESEventServiceConfiguration.SetParent, IESEventServiceConfiguration::SetParent, SetParent, SetParent method [Microsoft TV Technologies], SetParent method [Microsoft TV Technologies],IESEventServiceConfiguration interface, mstv.ieseventserviceconfiguration_setparent, tuner/IESEventServiceConfiguration::SetParent
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
 - IESEventServiceConfiguration::SetParent
 - tuner/IESEventServiceConfiguration::SetParent
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
 - IESEventServiceConfiguration.SetParent
---

# IESEventServiceConfiguration::SetParent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Sets a parent event service for an event service that implements the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a> interface. Once an event service has set a parent, it can receive advise events from the parent.

## -parameters

### -param pEventService [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a> interface for the parent event service.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventserviceconfiguration">IESEventServiceConfiguration</a>