---
UID: NF:tuner.IESEventServiceConfiguration.RemoveOwner
title: IESEventServiceConfiguration::RemoveOwner (tuner.h)
author: windows-sdk-content
description: Removes the owner of an event service, where event service refers to a generic Windows event service that implements the IESEventService interface.
old-location: mstv\ieseventserviceconfiguration_removeowner.htm
tech.root: mstv
ms.assetid: c55b732e-960c-4a0c-939b-2f3628b5c9b6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IESEventServiceConfiguration interface [Microsoft TV Technologies],RemoveOwner method, IESEventServiceConfiguration.RemoveOwner, IESEventServiceConfiguration::RemoveOwner, RemoveOwner, RemoveOwner method [Microsoft TV Technologies], RemoveOwner method [Microsoft TV Technologies],IESEventServiceConfiguration interface, mstv.ieseventserviceconfiguration_removeowner, tuner/IESEventServiceConfiguration::RemoveOwner
ms.topic: method
f1_keywords: 
 - "tuner/IESEventServiceConfiguration.RemoveOwner"
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
 - IESEventServiceConfiguration.RemoveOwner
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESEventServiceConfiguration::RemoveOwner


## -description


Removes the owner of an event service, where <i>event service</i> refers to a generic Windows event service that implements the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a> interface. The owner is the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevents">IESEvents</a> object that the parent event service uses to pass advise events to its child for handling.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventservice">IESEventService</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ieseventserviceconfiguration">IESEventServiceConfiguration</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventserviceconfiguration-setparent">SetParent</a>
 

 

