---
UID: NF:tuner.IESEventServiceConfiguration.RemoveParent
title: IESEventServiceConfiguration::RemoveParent (tuner.h)
description: Removes the parent of the current event service. Once an event service has removed a parent, the parent can no longer pass advise events to the child event service for handling.
old-location: mstv\ieseventserviceconfiguration_removeparent.htm
tech.root: mstv
ms.assetid: 74d92e84-9819-49ed-bd56-26d6768f3ed0
ms.date: 12/05/2018
ms.keywords: IESEventServiceConfiguration interface [Microsoft TV Technologies],RemoveParent method, IESEventServiceConfiguration.RemoveParent, IESEventServiceConfiguration::RemoveParent, RemoveParent, RemoveParent method [Microsoft TV Technologies], RemoveParent method [Microsoft TV Technologies],IESEventServiceConfiguration interface, mstv.ieseventserviceconfiguration_removeparent, tuner/IESEventServiceConfiguration::RemoveParent
f1_keywords:
- tuner/IESEventServiceConfiguration.RemoveParent
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
- IESEventServiceConfiguration.RemoveParent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESEventServiceConfiguration::RemoveParent


## -description


Removes the parent of the current event service. Once an event service has removed a parent, the parent can no longer pass advise events to the child event service for handling.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventserviceconfiguration">IESEventServiceConfiguration</a>
 

 

