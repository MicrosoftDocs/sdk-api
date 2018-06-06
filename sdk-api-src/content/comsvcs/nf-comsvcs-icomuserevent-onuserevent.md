---
UID: NF:comsvcs.IComUserEvent.OnUserEvent
title: IComUserEvent::OnUserEvent
author: windows-sdk-content
description: Provided for user components to generate user-defined events.
old-location: cos\icomuserevent_onuserevent.htm
old-project: cossdk
ms.assetid: 3c14bf53-7466-4cb0-b90f-681796e40fd3
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComUserEvent interface [COM+],OnUserEvent method, IComUserEvent.OnUserEvent, IComUserEvent::OnUserEvent, OnUserEvent, OnUserEvent method [COM+], OnUserEvent method [COM+],IComUserEvent interface, _dtc_IComUserEvent_OnUserEvent, comsvcs/IComUserEvent::OnUserEvent, cos.icomuserevent_onuserevent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComUserEvent.OnUserEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComUserEvent::OnUserEvent


## -description


Provided for user components to generate user-defined events.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param pvarEvent [in]

The user-defined information.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/a443b54a-018f-48a0-b61c-9e18e9567a22">IComUserEvent</a>
 

 

