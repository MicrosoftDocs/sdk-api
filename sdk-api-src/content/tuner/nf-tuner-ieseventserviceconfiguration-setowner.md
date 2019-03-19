---
UID: NF:tuner.IESEventServiceConfiguration.SetOwner
title: IESEventServiceConfiguration::SetOwner (tuner.h)
author: windows-sdk-content
description: Adds an owner to an event service, where event service refers to a generic Windows event service that implements the IESEventService interface.
old-location: mstv\ieseventserviceconfiguration_setowner.htm
tech.root: mstv
ms.assetid: 7d8e1be1-b363-41ac-b60b-98415f0f44b6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IESEventServiceConfiguration interface [Microsoft TV Technologies],SetOwner method, IESEventServiceConfiguration.SetOwner, IESEventServiceConfiguration::SetOwner, SetOwner, SetOwner method [Microsoft TV Technologies], SetOwner method [Microsoft TV Technologies],IESEventServiceConfiguration interface, mstv.ieseventserviceconfiguration_setowner, tuner/IESEventServiceConfiguration::SetOwner
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
 - IESEventServiceConfiguration.SetOwner
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IESEventServiceConfiguration::SetOwner


## -description


Adds an owner to an event service, where <i>event service</i> refers to a generic Windows event service that implements the <a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a> interface. The owner is the <a href="https://msdn.microsoft.com/1921f632-bb3b-4833-aa25-9caa3d65363f">IESEvents</a> object that the parent event service uses to pass advise events to its child event service for handling.


## -parameters




### -param pESEvents [in]

Pointer to the <a href="https://msdn.microsoft.com/1921f632-bb3b-4833-aa25-9caa3d65363f">IESEvents</a> interface that the  parent event service uses to advise its child.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b901732-42e1-4f50-904c-75d8202bb5b7">IESEventServiceConfiguration</a>



<a href="https://msdn.microsoft.com/1921f632-bb3b-4833-aa25-9caa3d65363f">IESEvents</a>



<a href="https://msdn.microsoft.com/cfb931e9-f20f-4812-9d6b-cf8b651b7e7a">SetParent</a>
 

 

