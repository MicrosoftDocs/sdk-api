---
UID: NF:tuner.IESEventServiceConfiguration.RemoveParent
title: IESEventServiceConfiguration::RemoveParent (tuner.h)
description: Removes the parent of the current event service. Once an event service has removed a parent, the parent can no longer pass advise events to the child event service for handling.
helpviewer_keywords: ["IESEventServiceConfiguration interface [Microsoft TV Technologies]","RemoveParent method","IESEventServiceConfiguration.RemoveParent","IESEventServiceConfiguration::RemoveParent","RemoveParent","RemoveParent method [Microsoft TV Technologies]","RemoveParent method [Microsoft TV Technologies]","IESEventServiceConfiguration interface","mstv.ieseventserviceconfiguration_removeparent","tuner/IESEventServiceConfiguration::RemoveParent"]
old-location: mstv\ieseventserviceconfiguration_removeparent.htm
tech.root: mstv
ms.assetid: 74d92e84-9819-49ed-bd56-26d6768f3ed0
ms.date: 12/05/2018
ms.keywords: IESEventServiceConfiguration interface [Microsoft TV Technologies],RemoveParent method, IESEventServiceConfiguration.RemoveParent, IESEventServiceConfiguration::RemoveParent, RemoveParent, RemoveParent method [Microsoft TV Technologies], RemoveParent method [Microsoft TV Technologies],IESEventServiceConfiguration interface, mstv.ieseventserviceconfiguration_removeparent, tuner/IESEventServiceConfiguration::RemoveParent
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
 - IESEventServiceConfiguration::RemoveParent
 - tuner/IESEventServiceConfiguration::RemoveParent
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
 - IESEventServiceConfiguration.RemoveParent
---

# IESEventServiceConfiguration::RemoveParent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Removes the parent of the current event service. Once an event service has removed a parent, the parent can no longer pass advise events to the child event service for handling.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventserviceconfiguration">IESEventServiceConfiguration</a>
