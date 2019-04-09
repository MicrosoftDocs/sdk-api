---
UID: NS:eventsys.__MIDL___MIDL_itf_eventsys_0000_0009_0001
title: COMEVENTSYSCHANGEINFO (eventsys.h)
author: windows-sdk-content
description: Represents a system event structure, which contains the partition and application ID from which an event originated.
old-location: cos\comeventsyschangeinfo.htm
tech.root: cossdk
ms.assetid: 6c9f143e-bdd4-48be-a635-a382c8c770c1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: COMEVENTSYSCHANGEINFO, COMEVENTSYSCHANGEINFO structure [COM+], _cos_COMEVENTSYSCHANGEINFO, cos.comeventsyschangeinfo, eventsys/COMEVENTSYSCHANGEINFO
ms.topic: struct
req.header: eventsys.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EventSys.h
api_name:
 - COMEVENTSYSCHANGEINFO
product: Windows
targetos: Windows
req.typenames: COMEVENTSYSCHANGEINFO
req.redist: 
---

# COMEVENTSYSCHANGEINFO structure


## -description


Represents a system event structure, which contains the partition and application ID from which an event originated.


## -struct-fields




### -field cbSize

The size of this structure.


### -field changeType

The type of change that has been made to the subscription. For a list of values, see <a href="https://msdn.microsoft.com/99a32590-6875-40ab-997a-c940b25b5de9">EOC_ChangeType</a>.


### -field objectId

The EventClass ID or subscription ID from which the change impacts.


### -field partitionId

The EventClass partition ID or the subscriber partition ID affected.


### -field applicationId

The EventClass application ID or subscriber application ID affected.


### -field reserved

This member is reserved.


## -see-also




<a href="https://msdn.microsoft.com/1b51c7ad-eae7-4030-81c2-ed9259648d31">IEventObjectChange2</a>
 

 

