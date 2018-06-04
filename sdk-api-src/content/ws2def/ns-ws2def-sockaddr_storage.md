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

# sockaddr_storage structure


## -description


The SOCKADDR_STORAGE structure is a generic structure that specifies a transport address.


## -struct-fields




### -field ss_family

The address family for the transport address. For more information about supported address
     families, see 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff571151">WSK Address Families</a>.


### -field __ss_pad1

A padding of 6 bytes that puts the 
     <b>__ss_align</b> member on an eight-byte boundary within the structure.


### -field __ss_align

A 64-bit value that forces the structure to be 8-byte aligned.


### -field __ss_pad2

A padding of an additional 112 bytes that brings the total size of the SOCKADDR_STORAGE structure
     to 128 bytes.


## -remarks



A WSK application typically does not directly access any of the members of the SOCKADDR_STORAGE
    structure except for the 
    <b>ss_family</b> member. Instead, a pointer to a SOCKADDR_STORAGE structure is normally cast to a pointer
    to the specific SOCKADDR structure type that corresponds to a particular address family.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a>
 

 

