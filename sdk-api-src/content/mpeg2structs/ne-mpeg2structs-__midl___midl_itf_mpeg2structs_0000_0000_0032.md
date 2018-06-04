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

# __MIDL___MIDL_itf_mpeg2structs_0000_0000_0032 enumeration


## -description



The <b>MPEG_REQUEST_TYPE</b> enumeration type specifies a request for MPEG-2 data.




## -enum-fields




### -field MPEG_RQST_UNKNOWN

Unknown request type. Do not use this value.


### -field MPEG_RQST_GET_SECTION

Get one table section. (Synchronous call.)


### -field MPEG_RQST_GET_SECTION_ASYNC

Get one table section. (Asynchronous call.)


### -field MPEG_RQST_GET_TABLE

Get a complete table. (Synchronous call.)


### -field MPEG_RQST_GET_TABLE_ASYNC

Get a complete table. (Asynchronous call.)


### -field MPEG_RQST_GET_SECTIONS_STREAM

Get a stream of sections.


### -field MPEG_RQST_GET_PES_STREAM

Get a stream of packetized elementary stream (PES) packets.


### -field MPEG_RQST_GET_TS_STREAM

Get a stream of transport stream (TS) packets.


### -field MPEG_RQST_START_MPE_STREAM

Get a stream of multi-protocol encapsulation (MPE) packets.


## -see-also




<a href="https://msdn.microsoft.com/13183e2a-6fbb-422c-b93c-53c12cb27423">BDA Enumeration Types</a>



<a href="https://msdn.microsoft.com/196abb62-97f6-4961-b843-895ae35fedc4">ISectionList::Initialize</a>
 

 

