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

# _IMAPI_FORMAT2_DATA_WRITE_ACTION enumeration


## -description


Defines values that indicate the current state of the write operation when using the <a href="https://msdn.microsoft.com/6bf149d3-62ea-4ef5-8d45-44df9ad4982c">IDiscFormat2DataEventArgs</a> interface.


## -enum-fields




### -field IMAPI_FORMAT2_DATA_WRITE_ACTION_VALIDATING_MEDIA

Validating that the current media is supported.


### -field IMAPI_FORMAT2_DATA_WRITE_ACTION_FORMATTING_MEDIA

Formatting media, when required.


### -field IMAPI_FORMAT2_DATA_WRITE_ACTION_INITIALIZING_HARDWARE

Initializing the hardware, for example, setting drive write speeds.


### -field IMAPI_FORMAT2_DATA_WRITE_ACTION_CALIBRATING_POWER

Optimizing laser intensity for writing to the media.


### -field IMAPI_FORMAT2_DATA_WRITE_ACTION_WRITING_DATA

Writing data to the media.


### -field IMAPI_FORMAT2_DATA_WRITE_ACTION_FINALIZATION

Finalizing the write.  This state is media dependent and can include items such as closing the track or session, or finishing background formatting.


### -field IMAPI_FORMAT2_DATA_WRITE_ACTION_COMPLETED

Successfully finished the write process.


### -field IMAPI_FORMAT2_DATA_WRITE_ACTION_VERIFYING

Verifying the integrity of the burned media.


## -see-also




<a href="https://msdn.microsoft.com/ad7db1a4-7ea8-46d7-8c4f-e7b9fb232f63">IDiscFormat2DataEventArgs::get_CurrentAction</a>
 

 

