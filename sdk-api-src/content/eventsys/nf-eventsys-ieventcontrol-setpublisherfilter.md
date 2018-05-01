---
UID: NF:eventsys.IEventControl.SetPublisherFilter
title: IEventControl::SetPublisherFilter method
author: windows-driver-content
description: Assigns a publisher filter to an event method.
old-location: cos\ieventcontrol_setpublisherfilter.htm
old-project: cossdk
ms.assetid: 9ebe0f55-9e2f-4538-9c16-1b237abfd07b
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IEventControl, IEventControl interface [COM+], SetPublisherFilter method, IEventControl::SetPublisherFilter, SetPublisherFilter method [COM+], SetPublisherFilter method [COM+], IEventControl interface, SetPublisherFilter,IEventControl.SetPublisherFilter, _cos_IEventControl_SetPublisherFilter, cos.ieventcontrol_setpublisherfilter, eventsys/IEventControl::SetPublisherFilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Eventsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EOC_ChangeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Eventsys.h
api_name:
-	IEventControl.SetPublisherFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventControl::SetPublisherFilter method


## -description


Assigns a publisher filter to an event method.


## -parameters




### -param methodName [in]

The name of the event method associated with the publisher filter to be assigned.


### -param pPublisherFilter [in]

A pointer to the <a href="https://msdn.microsoft.com/affc0af4-36f8-4479-8685-f91c29111d76">IPublisherFilter</a> interface on the publisher filter associated with the specified method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An event publisher can install a publisher filter at run time to fire an event only to subscribers that meet the criteria specified in the filter.




## -see-also




<a href="https://msdn.microsoft.com/8b2fba30-3ede-466f-ad3b-2de2175a088b">IEventControl</a>
 

 

