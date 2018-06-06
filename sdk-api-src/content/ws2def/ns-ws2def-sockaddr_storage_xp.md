---
UID: NS:ws2def.sockaddr_storage_xp
title: sockaddr_storage_xp
author: windows-sdk-content
description: The SOCKADDR_STORAGE structure is a generic structure that specifies a transport address.
old-location: netvista\sockaddr_storage.htm
old-project: netvista
ms.assetid: 27e56c1a-ce11-4cdb-9be8-25ed2f94fb37
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*LPSOCKADDR_STORAGE_XP, *PSOCKADDR_STORAGE, *PSOCKADDR_STORAGE_XP, FAR *LPSOCKADDR_STORAGE_LH, FAR *LPSOCKADDR_STORAGE_LH structure [Network Drivers Starting with Windows Vista], PSOCKADDR_STORAGE_LH, PSOCKADDR_STORAGE_LH structure pointer [Network Drivers Starting with Windows Vista], SOCKADDR_STORAGE, SOCKADDR_STORAGE structure [Network Drivers Starting with Windows Vista], SOCKADDR_STORAGE_LH, SOCKADDR_STORAGE_LH structure [Network Drivers Starting with Windows Vista], SOCKADDR_STORAGE_XP, netvista.sockaddr_storage, sockaddr_storage_xp, ws2def/FAR *LPSOCKADDR_STORAGE_LH, ws2def/PSOCKADDR_STORAGE_LH, ws2def/SOCKADDR_STORAGE, wskref_6daf4329-4069-419a-add7-dada30940663.xml"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ws2def.h
req.include-header: Wsk.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SOCKADDR_STORAGE_XP, *PSOCKADDR_STORAGE_XP, *LPSOCKADDR_STORAGE_XP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ws2def.h
api_name:
 - SOCKADDR_STORAGE_LH
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# sockaddr_storage_xp structure


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
 

 

