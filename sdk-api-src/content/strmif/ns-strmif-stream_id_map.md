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

# STREAM_ID_MAP structure


## -description



The <code>STREAM_ID_MAP</code> structure describes an elementary stream within an MPEG-2 program stream. Used with the <a href="https://msdn.microsoft.com/8bca9255-2bc8-408b-9127-e3fe050fcf01">IEnumStreamIdMap</a> interface methods.




## -struct-fields




### -field stream_id

Specifies the ID of the PES stream.


### -field dwMediaSampleContent

Specifies the media contents of the stream. May be one of the following values defined in axextend.idl:



#### MPEG2_PROGRAM_STREAM_MAP (0x00000000)



#### MPEG2_PROGRAM_ELEMENTARY_STREAM (0x00000001)



#### MPEG2_PROGRAM_DIRECTORY_PES_PACKET (0x00000002)



#### MPEG2_PROGRAM_PACK_HEADER (0x00000003)



#### MPEG2_PROGRAM_PES_STREAM (0x00000004)



#### MPEG2_PROGRAM_SYSTEM_HEADER (0x00000005)


### -field ulSubstreamFilterValue

Specifies the substream within the elementary stream. If no substream filtering is required, use SUBSTREAM_FILTER_VAL_NONE (0x10000000).


### -field iDataOffset

Specifies the offset in bytes for the substream. If no filtering is required, specify 0.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

