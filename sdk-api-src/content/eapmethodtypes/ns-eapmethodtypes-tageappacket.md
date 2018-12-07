---
UID: NS:eapmethodtypes.tagEapPacket
title: tagEapPacket
author: windows-sdk-content
description: Contains a packet of opaque data sent during an EAP authentication session.
old-location: eaphost\eappacket.htm
tech.root: eaphost
ms.assetid: a5d78db0-990f-4318-8f1a-4e903221845f
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: EapPacket, EapPacket structure [EAPHost], eaphost.eappacket, eapmethodtypes/EapPacket, tagEapPacket
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: eapmethodtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - eapmethodtypes.h
api_name:
 - EapPacket
product: Windows
targetos: Windows
req.typenames: EapPacket
req.redist: 
---

# tagEapPacket structure


## -description


 The <b>EapPacket</b> structure contains a packet of opaque data sent during an EAP authentication session.


## -struct-fields




### -field Code

An <a href="https://msdn.microsoft.com/19d424a1-91d6-4ebd-acb8-912b4900a4cd">EapCode</a> enumeration value that identifies the packet type.


### -field Id

The packet ID number.


### -field Length

The length of the entire packet


### -field Data

The packet message data. This opaque data block continues after the first byte for <b>Length</b> - 1 bytes.


## -see-also




<a href="https://msdn.microsoft.com/f6f3b909-1e89-47f8-853c-c0f3f2414817">Common EAPHost API Structures</a>



<a href="https://msdn.microsoft.com/19d424a1-91d6-4ebd-acb8-912b4900a4cd">EapCode</a>
 

 

