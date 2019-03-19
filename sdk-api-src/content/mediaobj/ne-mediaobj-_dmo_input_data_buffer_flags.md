---
UID: NE:mediaobj._DMO_INPUT_DATA_BUFFER_FLAGS
title: "_DMO_INPUT_DATA_BUFFER_FLAGS" (mediaobj.h)
author: windows-sdk-content
description: The DMO_INPUT_DATA_BUFFER_FLAGS enumeration defines flags that describe an input buffer.
old-location: dshow\dmo_input_data_buffer_flags.htm
tech.root: DirectShow
ms.assetid: b0217926-ac2d-48e5-a5d0-e31be6ea20ac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DMO_INPUT_DATA_BUFFERF_SYNCPOINT, DMO_INPUT_DATA_BUFFERF_TIME, DMO_INPUT_DATA_BUFFERF_TIMELENGTH, DMO_INPUT_DATA_BUFFER_FLAGS , DMO_INPUT_DATA_BUFFER_FLAGSEnumeration, _DMO_INPUT_DATA_BUFFER_FLAGS, _DMO_INPUT_DATA_BUFFER_FLAGS enumeration [DirectShow], dshow.dmo_input_data_buffer_flags, mediaobj/DMO_INPUT_DATA_BUFFERF_SYNCPOINT, mediaobj/DMO_INPUT_DATA_BUFFERF_TIME, mediaobj/DMO_INPUT_DATA_BUFFERF_TIMELENGTH, mediaobj/_DMO_INPUT_DATA_BUFFER_FLAGS
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mediaobj.h
api_name:
 - _DMO_INPUT_DATA_BUFFER_FLAGS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _DMO_INPUT_DATA_BUFFER_FLAGS enumeration


## -description



The <code>DMO_INPUT_DATA_BUFFER_FLAGS</code> enumeration defines flags that describe an input buffer.




## -enum-fields




### -field DMO_INPUT_DATA_BUFFERF_SYNCPOINT

The beginning of the data is a synchronization point.


### -field DMO_INPUT_DATA_BUFFERF_TIME

The buffer's time stamp is valid.

The buffer's indicated time length is valid.


### -field DMO_INPUT_DATA_BUFFERF_TIMELENGTH

The buffer's indicated time length is valid.


### -field DMO_INPUT_DATA_BUFFERF_DISCONTINUITY




## -see-also




<a href="https://msdn.microsoft.com/5d60c902-5fb0-419b-b54d-5e3b543c5df8">DMO Enumerated Types</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406959(v=VS.85).aspx">IMediaObject::ProcessInput</a>
 

 

