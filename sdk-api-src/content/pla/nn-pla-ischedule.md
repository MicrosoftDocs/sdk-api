---
UID: NN:pla.ISchedule
title: ISchedule
author: windows-sdk-content
description: Specifies when the data collector set runs.To get this interface, call the IScheduleCollection::CreateSchedule method.
old-location: pla\ischedule.htm
tech.root: PLA
ms.assetid: b02043c6-5010-45a1-a4a4-ce30cbf0dba0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISchedule, ISchedule interface [PLA], ISchedule interface [PLA],described, base.ischedule, pla.ischedule, pla/ISchedule
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ISchedule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISchedule interface


## -description


Specifies when the data collector set runs.

To get this interface, call the <a href="https://msdn.microsoft.com/8fa10cd9-d1ae-47c7-80e2-416165164491">IScheduleCollection::CreateSchedule</a> method.


## -remarks



To create the object from a script, use the Pla.Schedule program identifier.

PLA uses the schedule when the <a href="https://msdn.microsoft.com/75ebe328-1494-464c-9491-e8a39e1d8ee1">IDataCollectorSet::SchedulesEnabled</a> property is VARIANT_TRUE.

For an example that shows the XML that you can use to initialize this object if you call the <a href="https://msdn.microsoft.com/10bffd54-990f-412f-baae-b8ab621b02b8">IDataCollectorSet::SetXml</a> method, see the Remarks section of <a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>.  When you specify the XML to create the object, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the set, the XML includes all elements. 



