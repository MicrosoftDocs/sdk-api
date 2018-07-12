---
UID: NS:ws2def._SOCKET_PROCESSOR_AFFINITY
title: "_SOCKET_PROCESSOR_AFFINITY"
author: windows-sdk-content
description: Contains the association between a socket and an RSS processor core and NUMA node.
old-location: winsock\socket_processor_affinity.htm
old-project: WinSock
ms.assetid: CB1E9F79-C6BD-40C2-8D0F-36B24B1BBBF4
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*PSOCKET_PROCESSOR_AFFINITY, PSOCKET_PROCESSOR_AFFINITY, PSOCKET_PROCESSOR_AFFINITY structure pointer [Winsock], SOCKET_PROCESSOR_AFFINITY, SOCKET_PROCESSOR_AFFINITY structure [Winsock], _SOCKET_PROCESSOR_AFFINITY, winsock.socket_processor_affinity, ws2def/PSOCKET_PROCESSOR_AFFINITY, ws2def/SOCKET_PROCESSOR_AFFINITY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ws2def.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: SOCKET_PROCESSOR_AFFINITY, *PSOCKET_PROCESSOR_AFFINITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2def.h
api_name:
 - SOCKET_PROCESSOR_AFFINITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SOCKET_PROCESSOR_AFFINITY structure


## -description


The <b>SOCKET_PROCESSOR_AFFINITY</b> structure contains the association between a socket and an RSS processor core and NUMA node..


## -struct-fields




### -field Processor

A structure to represent a system wide processor number. This <a href="https://msdn.microsoft.com/library/windows/hardware/ff559913">PROCESSOR_NUMBER</a> structure contains a
group number and relative processor number within the group.


### -field NumaNodeId

The NUMA node ID.


### -field Reserved

A value reserved for future use.


## -remarks



The <b>SOCKET_PROCESSOR_AFFINITY</b>  structure is supported on Windows 8,   and Windows Server 2012, and later versions of the operating system.

The <a href="https://msdn.microsoft.com/DAF18C92-B479-474F-B438-0746CBA20653">SIO_QUERY_RSS_PROCESSOR_INFO</a> 
        IOCTL is used to determine the association between a socket and an RSS processor core and NUMA node. This IOCTL returns a <b>SOCKET_PROCESSOR_AFFINITY</b> structure that contains the processor number and the NUMA node ID.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff559913">PROCESSOR_NUMBER</a>



<a href="https://msdn.microsoft.com/DAF18C92-B479-474F-B438-0746CBA20653">SIO_QUERY_RSS_PROCESSOR_INFO</a>
 

 

