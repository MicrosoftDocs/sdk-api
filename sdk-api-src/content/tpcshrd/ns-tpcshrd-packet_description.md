---
UID: NS:tpcshrd._PACKET_DESCRIPTION
title: PACKET_DESCRIPTION (tpcshrd.h)
description: Describes the content of the packet for a particular tablet recognizer context.Do not use this structure to access the data contained in a packet. This structure describes the content of the packet.
helpviewer_keywords: ["*PPACKET_DESCRIPTION","6823f2c6-2c99-4b9a-8208-041fc1f7bf82","PACKET_DESCRIPTION","PACKET_DESCRIPTION structure [Tablet PC]","PPACKET_DESCRIPTION","PPACKET_DESCRIPTION structure pointer [Tablet PC]","tablet.packet_description","tpcshrd/PACKET_DESCRIPTION","tpcshrd/PPACKET_DESCRIPTION"]
old-location: tablet\packet_description.htm
tech.root: tablet
ms.assetid: 6823f2c6-2c99-4b9a-8208-041fc1f7bf82
ms.date: 12/05/2018
ms.keywords: '*PPACKET_DESCRIPTION, 6823f2c6-2c99-4b9a-8208-041fc1f7bf82, PACKET_DESCRIPTION, PACKET_DESCRIPTION structure [Tablet PC], PPACKET_DESCRIPTION, PPACKET_DESCRIPTION structure pointer [Tablet PC], tablet.packet_description, tpcshrd/PACKET_DESCRIPTION, tpcshrd/PPACKET_DESCRIPTION'
req.header: tpcshrd.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PACKET_DESCRIPTION, *PPACKET_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PACKET_DESCRIPTION
 - tpcshrd/_PACKET_DESCRIPTION
 - PPACKET_DESCRIPTION
 - tpcshrd/PPACKET_DESCRIPTION
 - PACKET_DESCRIPTION
 - tpcshrd/PACKET_DESCRIPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tpcshrd.h
api_name:
 - PACKET_DESCRIPTION
---

# PACKET_DESCRIPTION structure


## -description

Describes the content of the packet for a particular tablet recognizer context.

Do not use this structure to access the data contained in a packet. This structure describes the content of the packet.

## -struct-fields

### -field cbPacketSize

The size, in bytes, of the packet data.

### -field cPacketProperties

The number of elements in the <i>pPacketProperties</i> array.

### -field pPacketProperties

An array of <a href="/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property">PACKET_PROPERTY</a> structures.

### -field cButtons

Deprecated. Do not use.

### -field pguidButtons

Deprecated. Do not use.

## -remarks

The <b>PACKET_DESCRIPTION</b> structure defines the logical layout of the packet. Typically, you do not need to address the contents of a packet. You pass the packets to the Ink object. However, if you need to address the contents of a packet, each packet contains a series of LONG values (properties) followed by one or more DWORD values (button states).

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-addstroke">AddStroke Function</a>



<a href="/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription">GetPreferredPacketDescription Function</a>