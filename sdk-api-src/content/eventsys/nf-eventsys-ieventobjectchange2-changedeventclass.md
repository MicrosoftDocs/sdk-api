---
UID: NF:eventsys.IEventObjectChange2.ChangedEventClass
title: IEventObjectChange2::ChangedEventClass
author: windows-sdk-content
description: Indicates that an event class object has been added, modified, or deleted.
old-location: cos\ieventobjectchange2_changedeventclass.htm
old-project: cossdk
ms.assetid: ae760225-2c4f-46e5-8d35-eefec8f2f5da
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ChangedEventClass, ChangedEventClass method [COM+], ChangedEventClass method [COM+],IEventObjectChange2 interface, IEventObjectChange2 interface [COM+],ChangedEventClass method, IEventObjectChange2.ChangedEventClass, IEventObjectChange2::ChangedEventClass, _cos_ieventobjectchange2_changedeventclass, cos.ieventobjectchange2_changedeventclass, eventsys/IEventObjectChange2::ChangedEventClass
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EOC_ChangeType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Eventsys.h
api_name:
 - IEventObjectChange2.ChangedEventClass
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventObjectChange2::ChangedEventClass


## -description



Indicates that an event class object has been added, modified, or deleted.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/6c9f143e-bdd4-48be-a635-a382c8c770c1">COMEVENTSYSCHANGEINFO</a> structure. 


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/1b51c7ad-eae7-4030-81c2-ed9259648d31">IEventObjectChange2</a>
 

 

