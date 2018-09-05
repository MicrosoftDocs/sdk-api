---
UID: NS:tpcshrd._PACKET_DESCRIPTION
title: "_PACKET_DESCRIPTION"
author: windows-sdk-content
description: Describes the content of the packet for a particular tablet recognizer context.Do not use this structure to access the data contained in a packet. This structure describes the content of the packet.
old-location: tablet\packet_description.htm
old-project: tablet
ms.assetid: 6823f2c6-2c99-4b9a-8208-041fc1f7bf82
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: "*PPACKET_DESCRIPTION, 6823f2c6-2c99-4b9a-8208-041fc1f7bf82, PACKET_DESCRIPTION, PACKET_DESCRIPTION structure [Tablet PC], PPACKET_DESCRIPTION, PPACKET_DESCRIPTION structure pointer [Tablet PC], _PACKET_DESCRIPTION, tablet.packet_description, tpcshrd/PACKET_DESCRIPTION, tpcshrd/PPACKET_DESCRIPTION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tpcshrd.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: PACKET_DESCRIPTION, *PPACKET_DESCRIPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tpcshrd.h
api_name:
 - PACKET_DESCRIPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

