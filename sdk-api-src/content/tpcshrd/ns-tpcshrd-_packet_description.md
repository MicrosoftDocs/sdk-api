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

# _PACKET_DESCRIPTION structure


## -description



Describes the content of the packet for a particular tablet recognizer context.

Do not use this structure to access the data contained in a packet. This structure describes the content of the packet.




## -struct-fields




### -field cbPacketSize

The size, in bytes, of the packet data.


### -field cPacketProperties

The number of elements in the <i>pPacketProperties</i> array.


### -field pPacketProperties

An array of <a href="https://msdn.microsoft.com/c1bd6240-7f95-421c-8622-0d7b98182d7c">PACKET_PROPERTY</a> structures.


### -field cButtons

Deprecated. Do not use.


### -field pguidButtons

Deprecated. Do not use.


## -remarks



The <b>PACKET_DESCRIPTION</b> structure defines the logical layout of the packet. Typically, you do not need to address the contents of a packet. You pass the packets to the Ink object. However, if you need to address the contents of a packet, each packet contains a series of LONG values (properties) followed by one or more DWORD values (button states).




## -see-also




<a href="https://msdn.microsoft.com/1db3dbef-41bf-4b00-8e6c-07c7c414e595">AddStroke Function</a>



<a href="https://msdn.microsoft.com/6600b345-db7a-49ca-a54a-7d212952cb8f">GetPreferredPacketDescription Function</a>
 

 

