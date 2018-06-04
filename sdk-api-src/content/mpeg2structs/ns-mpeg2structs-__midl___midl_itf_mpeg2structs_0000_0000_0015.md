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

# __MIDL___MIDL_itf_mpeg2structs_0000_0000_0015 structure


## -description



The <b>MPEG_PACKET_LIST</b> structure contains a list of MPEG-2 sections.




## -struct-fields




### -field wPacketCount

Specifies the size of the <b>PacketList</b> array.


### -field PacketList

Specifies a pointer to an array of <a href="https://msdn.microsoft.com/b7777633-66c3-44c2-9cdb-14c540555a43">MPEG_RQST_PACKET</a> structures, which themselves contain pointers to buffers that hold the sectioned data.


## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>



<a href="https://msdn.microsoft.com/d376af4c-4b22-4a2d-917a-6f25d2c38861">MPEG_STREAM_BUFFER Structure</a>
 

 

