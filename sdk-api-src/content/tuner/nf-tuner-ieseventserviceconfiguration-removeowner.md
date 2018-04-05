---
UID: NF:tuner.IESEventServiceConfiguration.RemoveOwner
title: IESEventServiceConfiguration::RemoveOwner method
author: windows-driver-content
description: Removes the owner of an event service, where event service refers to a generic Windows event service that implements the IESEventService interface.
old-location: mstv\ieseventserviceconfiguration_removeowner.htm
old-project: mstv
ms.assetid: c55b732e-960c-4a0c-939b-2f3628b5c9b6
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IESEventServiceConfiguration, IESEventServiceConfiguration interface [Microsoft TV Technologies], RemoveOwner method, IESEventServiceConfiguration::RemoveOwner, RemoveOwner method [Microsoft TV Technologies], RemoveOwner method [Microsoft TV Technologies], IESEventServiceConfiguration interface, RemoveOwner,IESEventServiceConfiguration.RemoveOwner, mstv.ieseventserviceconfiguration_removeowner, tuner/IESEventServiceConfiguration::RemoveOwner
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IESEventServiceConfiguration.RemoveOwner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESEventServiceConfiguration::RemoveOwner method


## -description


Removes the owner of an event service, where <i>event service</i> refers to a generic Windows event service that implements the <a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a> interface. The owner is the <a href="https://msdn.microsoft.com/1921f632-bb3b-4833-aa25-9caa3d65363f">IESEvents</a> object that the parent event service uses to pass advise events to its child for handling.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2720d616-18a6-488e-98ef-565768c22c2a">IESEventService</a>



<a href="https://msdn.microsoft.com/0b901732-42e1-4f50-904c-75d8202bb5b7">IESEventServiceConfiguration</a>



<a href="https://msdn.microsoft.com/cfb931e9-f20f-4812-9d6b-cf8b651b7e7a">SetParent</a>
 

 

