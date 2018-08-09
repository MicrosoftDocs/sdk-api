---
UID: NE:mediaobj._DMO_OUTPUT_DATA_BUFFER_FLAGS
title: "_DMO_OUTPUT_DATA_BUFFER_FLAGS"
author: windows-sdk-content
description: The DMO_OUTPUT_DATA_BUFFER_FLAGS enumeration defines flags that describe an output buffer.
old-location: dshow\dmo_output_data_buffer_flags.htm
old-project: DirectShow
ms.assetid: 80ce44a7-4b69-4aed-8b28-10e84a658f12
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: DMO_OUTPUT_DATA_BUFFERF_INCOMPLETE, DMO_OUTPUT_DATA_BUFFERF_SYNCPOINT, DMO_OUTPUT_DATA_BUFFERF_TIME, DMO_OUTPUT_DATA_BUFFERF_TIMELENGTH, DMO_OUTPUT_DATA_BUFFER_FLAGS , DMO_OUTPUT_DATA_BUFFER_FLAGSEnumeration, _DMO_OUTPUT_DATA_BUFFER_FLAGS, _DMO_OUTPUT_DATA_BUFFER_FLAGS enumeration [DirectShow], dshow.dmo_output_data_buffer_flags, mediaobj/DMO_OUTPUT_DATA_BUFFERF_INCOMPLETE, mediaobj/DMO_OUTPUT_DATA_BUFFERF_SYNCPOINT, mediaobj/DMO_OUTPUT_DATA_BUFFERF_TIME, mediaobj/DMO_OUTPUT_DATA_BUFFERF_TIMELENGTH, mediaobj/_DMO_OUTPUT_DATA_BUFFER_FLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mediaobj.h
api_name:
 - _DMO_OUTPUT_DATA_BUFFER_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DMO_OUTPUT_DATA_BUFFER_FLAGS enumeration


## -description



The <b>DMO_OUTPUT_DATA_BUFFER_FLAGS</b> enumeration defines flags that describe an output buffer.




## -enum-fields




### -field DMO_OUTPUT_DATA_BUFFERF_SYNCPOINT

The beginning of the data is a synchronization point.
          A <i>synchronization point</i> is a random access point. For encoded video, this a sample that can be used as a decoding start point (key frame). For uncompressed audio or video, every sample is a synchronization point.


### -field DMO_OUTPUT_DATA_BUFFERF_TIME

The buffer's time stamp is valid.

The buffer's indicated time length is valid.
          


### -field DMO_OUTPUT_DATA_BUFFERF_TIMELENGTH

The buffer's indicated time length is valid.
          


### -field DMO_OUTPUT_DATA_BUFFERF_DISCONTINUITY


### -field DMO_OUTPUT_DATA_BUFFERF_INCOMPLETE

There is still input data available for processing, but the output buffer is full.
          


## -see-also




<a href="https://msdn.microsoft.com/5d60c902-5fb0-419b-b54d-5e3b543c5df8">DMO Enumerated Types</a>



<a href="https://msdn.microsoft.com/1a3b1192-f1e9-4f04-b543-d38692502b8e">IMediaObject::ProcessOutput</a>
 

 

