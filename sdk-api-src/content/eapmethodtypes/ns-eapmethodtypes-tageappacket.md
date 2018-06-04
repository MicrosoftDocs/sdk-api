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
 

 

