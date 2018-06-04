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
 

 

