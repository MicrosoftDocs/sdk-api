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

# __MIDL___MIDL_itf_mpeg2structs_0000_0000_0030 structure


## -description



The <b>MPEG_CONTEXT</b> structure identifies the source of an MPEG-2 data stream.




## -struct-fields




### -field Type

Specifies the source type, as an <a href="https://msdn.microsoft.com/cb76873e-78d0-4fd2-9caa-bff4ae250073">MPEG_CONTEXT_TYPE</a> value. Currently, the value must be MPEG_CONTEXT_BCS_DEMUX.


### -field U

A union that contains the following members.


### -field U.Demux

Specifies an <a href="https://msdn.microsoft.com/ecc4f3bb-16f5-4398-bcd5-3316da8529ec">MPEG_BCS_DEMUX</a> structure that identifies the filter graph instance.


### -field U.Winsock

Currently not supported.


## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>
 

 

