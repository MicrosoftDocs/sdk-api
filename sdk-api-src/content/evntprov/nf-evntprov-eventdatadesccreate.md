---
UID: NF:evntprov.EventDataDescCreate
title: EventDataDescCreate function
author: windows-sdk-content
description: Sets the values of an event data descriptor.
old-location: etw\eventdatadesccreate_func.htm
tech.root: ETW
ms.assetid: a5823ad0-0710-4fd2-9b44-a60a42f138fd
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EventDataDescCreate, EventDataDescCreate function [ETW], base.eventdatadesccreate_func, etw.eventdatadesccreate_func, evntprov/EventDataDescCreate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: evntprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - Evntprov.h
api_name:
 - EventDataDescCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EventDataDescCreate function


## -description


Sets the values of an event data descriptor.
		
		
	
	


## -parameters




### -param EventDataDescriptor [out]

The data descriptor whose member values are set to those of the remaining parameters. For details, see <a href="https://msdn.microsoft.com/452ce6f6-3857-4f88-b501-44dd6091b97e">EVENT_DATA_DESCRIPTOR</a>.


### -param DataPtr [in]

A pointer to the event data used to set the <b>Ptr</b> member of <a href="https://msdn.microsoft.com/452ce6f6-3857-4f88-b501-44dd6091b97e">EVENT_DATA_DESCRIPTOR</a>.

If the event data's type is a <b>NULL</b>-terminated string, the <i>DataPtr</i> parameter must not be <b>NULL</b>.

 If the event data's type  is a string whose size is described by some other field in the event, the <i>DataPtr</i> parameter may be <b>NULL</b>.


### -param DataSize [in]

The size of the event data. The value is used to set the <b>Size</b> member of <a href="https://msdn.microsoft.com/452ce6f6-3857-4f88-b501-44dd6091b97e">EVENT_DATA_DESCRIPTOR</a>.


## -returns



This function does not return a value.




## -remarks



This is a convenience macro for setting the members of the <a href="https://msdn.microsoft.com/452ce6f6-3857-4f88-b501-44dd6091b97e">EVENT_DATA_DESCRIPTOR</a> structure.



