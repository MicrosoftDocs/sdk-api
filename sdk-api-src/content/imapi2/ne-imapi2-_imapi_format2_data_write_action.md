---
UID: NE:imapi2._IMAPI_FORMAT2_DATA_WRITE_ACTION
title: "_IMAPI_FORMAT2_DATA_WRITE_ACTION"
author: windows-sdk-content
description: Defines values that indicate the current state of the write operation when using the IDiscFormat2DataEventArgs interface.
old-location: imapi\imapi_format2_data_write_action.htm
tech.root: imapi
ms.assetid: f406e727-e168-46d9-9c03-c949469bb1c9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PIMAPI_FORMAT2_DATA_WRITE_ACTION, IMAPI_FORMAT2_DATA_WRITE_ACTION, IMAPI_FORMAT2_DATA_WRITE_ACTION enumeration [IMAPI], IMAPI_FORMAT2_DATA_WRITE_ACTION_CALIBRATING_POWER, IMAPI_FORMAT2_DATA_WRITE_ACTION_COMPLETED, IMAPI_FORMAT2_DATA_WRITE_ACTION_FINALIZATION, IMAPI_FORMAT2_DATA_WRITE_ACTION_FORMATTING_MEDIA, IMAPI_FORMAT2_DATA_WRITE_ACTION_INITIALIZING_HARDWARE, IMAPI_FORMAT2_DATA_WRITE_ACTION_VALIDATING_MEDIA, IMAPI_FORMAT2_DATA_WRITE_ACTION_VERIFYING, IMAPI_FORMAT2_DATA_WRITE_ACTION_WRITING_DATA, PIMAPI_FORMAT2_DATA_WRITE_ACTION, PIMAPI_FORMAT2_DATA_WRITE_ACTION enumeration pointer [IMAPI], _IMAPI_FORMAT2_DATA_WRITE_ACTION, imapi.imapi_format2_data_write_action, imapi2/IMAPI_FORMAT2_DATA_WRITE_ACTION, imapi2/IMAPI_FORMAT2_DATA_WRITE_ACTION_CALIBRATING_POWER, imapi2/IMAPI_FORMAT2_DATA_WRITE_ACTION_COMPLETED, imapi2/IMAPI_FORMAT2_DATA_WRITE_ACTION_FINALIZATION, imapi2/IMAPI_FORMAT2_DATA_WRITE_ACTION_FORMATTING_MEDIA, imapi2/IMAPI_FORMAT2_DATA_WRITE_ACTION_INITIALIZING_HARDWARE, imapi2/IMAPI_FORMAT2_DATA_WRITE_ACTION_VALIDATING_MEDIA, imapi2/IMAPI_FORMAT2_DATA_WRITE_ACTION_VERIFYING, imapi2/IMAPI_FORMAT2_DATA_WRITE_ACTION_WRITING_DATA, imapi2/PIMAPI_FORMAT2_DATA_WRITE_ACTION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IMAPI_FORMAT2_DATA_WRITE_ACTION
product: Windows
targetos: Windows
req.typenames: IMAPI_FORMAT2_DATA_WRITE_ACTION, *PIMAPI_FORMAT2_DATA_WRITE_ACTION
req.redist: 
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
 

 

