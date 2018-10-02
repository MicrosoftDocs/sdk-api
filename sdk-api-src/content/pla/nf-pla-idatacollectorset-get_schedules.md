---
UID: NF:pla.IDataCollectorSet.get_Schedules
title: IDataCollectorSet::get_Schedules
author: windows-sdk-content
description: Retrieves the list of schedules that determine when the data collector set runs.
old-location: pla\idatacollectorset_get_schedules.htm
tech.root: PLA
ms.assetid: 6654c101-5179-41db-8fd9-ae281691073f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDataCollectorSet interface [PLA],Schedules property, IDataCollectorSet.Schedules, IDataCollectorSet.get_Schedules, IDataCollectorSet::Schedules, IDataCollectorSet::get_Schedules, Schedules property [PLA], Schedules property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_schedules, get_Schedules, pla.idatacollectorset_get_schedules, pla/IDataCollectorSet::Schedules, pla/IDataCollectorSet::get_Schedules
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.Schedules
 - IDataCollectorSet.get_Schedules
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollectorSet::get_Schedules


## -description


Retrieves the list of schedules that determine when the data collector set runs.

This property is read-only.


## -parameters


## -remarks



There can be only one instance of a data collector set running at a time; if one is already running and a second one tries to start, the second one will fail and the first one will continue.

To enable the schedules, call the <a href="https://msdn.microsoft.com/75ebe328-1494-464c-9491-e8a39e1d8ee1">IDataCollectorSet::SchedulesEnabled</a> property.

To manually start the data collector set, call the <a href="https://msdn.microsoft.com/63f0c7b7-0dc6-4491-a2f5-eaae9d22da61">IDataCollectorSet::Start</a> method.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/75ebe328-1494-464c-9491-e8a39e1d8ee1">IDataCollectorSet::SchedulesEnabled</a>
 

 

