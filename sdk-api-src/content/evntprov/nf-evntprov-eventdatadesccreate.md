---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



