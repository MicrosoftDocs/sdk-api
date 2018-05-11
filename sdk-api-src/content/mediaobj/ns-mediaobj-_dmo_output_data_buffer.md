---
UID: NS:mediaobj._DMO_OUTPUT_DATA_BUFFER
title: "_DMO_OUTPUT_DATA_BUFFER"
author: windows-driver-content
description: The DMO_OUTPUT_DATA_BUFFER structure describes an output buffer used by a Microsoft DirectX Media Object (DMO).
old-location: dshow\dmo_output_data_buffer.htm
old-project: DirectShow
ms.assetid: 87fa2000-8dab-4f30-940a-14fb6699f616
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PDMO_OUTPUT_DATA_BUFFER, DMO_OUTPUT_DATA_BUFFER, DMO_OUTPUT_DATA_BUFFER structure [DirectShow], DMO_OUTPUT_DATA_BUFFERStructure, PDMO_OUTPUT_DATA_BUFFER, PDMO_OUTPUT_DATA_BUFFER structure pointer [DirectShow], _DMO_OUTPUT_DATA_BUFFER, dshow.dmo_output_data_buffer, mediaobj/DMO_OUTPUT_DATA_BUFFER, mediaobj/PDMO_OUTPUT_DATA_BUFFER"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mediaobj.h
req.include-header: 
req.target-type: Windows
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
req.typenames: DMO_OUTPUT_DATA_BUFFER, *PDMO_OUTPUT_DATA_BUFFER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mediaobj.h
api_name:
-	DMO_OUTPUT_DATA_BUFFER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DMO_OUTPUT_DATA_BUFFER structure


## -description



The <code>DMO_OUTPUT_DATA_BUFFER</code> structure describes an output buffer used by a Microsoft DirectX Media Object (DMO).




## -struct-fields




### -field pBuffer

Pointer to the <a href="https://msdn.microsoft.com/74d72ca6-f899-43fc-bdea-5208d920f314">IMediaBuffer</a> interface of a buffer allocated by the application.


### -field dwStatus

Status flags. After processing output, the DMO sets this member to a bitwise combination of zero or more <a href="https://msdn.microsoft.com/80ce44a7-4b69-4aed-8b28-10e84a658f12">DMO_OUTPUT_DATA_BUFFER_FLAGS</a> flags.


### -field rtTimestamp

Time stamp that specifies the start time of the data in the buffer. If the buffer has a valid time stamp, the DMO sets this member and also sets the DMO_OUTPUT_DATA_BUFFERF_TIME flag in the <b>dwStatus</b> member. Otherwise, ignore this member.


### -field rtTimelength

Reference time specifying the length of the data in the buffer. If the DMO sets this member to a valid value, it also sets the DMO_OUTPUT_DATA_BUFFERF_TIMELENGTH flag in the <b>dwStatus</b> member. Otherwise, ignore this member.


## -see-also




<a href="https://msdn.microsoft.com/82c8ea74-1c5e-4370-9075-6db2ed6b2c91">DMO Structures</a>



<a href="https://msdn.microsoft.com/1a3b1192-f1e9-4f04-b543-d38692502b8e">IMediaObject::ProcessOutput</a>
 

 

